---
layout:     post
title:      理解MobileNetV2
subtitle:   
date:       2020-09-28
author:     Chao Xu
header-style: text
hidden: true
mathjax: true 
catalog: true
tags:
    - Image Segmentation
---

# 一、V2与V1的架构区别

和MobielNetV1相比，[MobileNet V2](https://arxiv.org/abs/1801.04381) 仍使用深度可分离卷积，但其主要构成模块如下图1所示：

<p align = "center">
    <img src = "https://machinethink.net/images/mobilenet-v2/ResidualBlock@2x.png" width = "300pix">
    图1（源自Ref [2]）
</p>


这次block中有三个卷积层，作者分别将其称之为**1 x 1 expansion layer**、**3 x 3 depthwise convolution**和**1 x 1 projection layer**。后两层其实就是V1中的depthwise convolution和1×1 pointwise convolution layer，只不过在V2中，作者后者称为1 x 1 projection layer，并有不同的作用。下面就来看看，两者的差异究竟在哪里。

在V1中，逐点卷积要么使通道数保持不变，要么使通道数翻倍。 在V2中，情况恰恰相反：它使通道数变小。 这就是为什么现在将该层称为投影层( Projection Layer)的原因：它将具有大量维（通道）的数据投影到具有较少维数的张量中。

>  例如，depthwise convolution可以在具有144个通道的张量上工作，然后projection layer张量缩小至24个通道。这种层也称为**bottleneck layer**，因为它减少了流经网络的数据量。（这就体现了“bottleneck residual block”名称的一部分：每个块的输出都是瓶颈。）

此外，bottleneck residual block的第一层是新出现的，也就是**expansion layer**。 它也是1×1卷积， 其目的是在数据进入深度卷积之前扩展数据中的通道数。 因此，expansion layer始终具有比输入通道更多的输出通道（与projection layer相反）。

Expansion layer将通道数扩展多少倍，这个由扩展因子(**expansion factor**)给出。 这也是调整不同架构的超参数之一， 默认扩展因子为6。

> 例如图2所示，如果有一个具有24个通道的张量进入一个bottleneck residual block，则expansion layer首先将其转换为具有24 x 6 = 144个通道的新张量。 接下来，depthwise convolution将其滤波器应用于该144通道张量。 最后，projection layer将144个过滤后的通道投影回较小的数量，比如说24个。

<p align = "center">
<img src = "https://machinethink.net/images/mobilenet-v2/ExpandProject@2x.png" height = "150pix">
图2（源自Ref [2]）                                                                                     </p>                                                                                                

因此，bottleneck residual block的输入和输出是低维张量，而block内发生的滤波步骤是在高维张量上完成的。

> 思考一下，这样做的好处是什么？

Bottleneck residual block体现了其还存在另一部分，那就是逆残差连接(**inverted residual connection**)，这也是MobileNetV2与MobileNetV1的不同之处。就像在ResNet中一样，它的存在是为了帮助梯度流过网络。只有当进入block的通道数与从block出来的通道数相同时（如图2），才使用**inverted residual connection，但并非总是如此，因为每隔几个块输出通道就增加一次。

一般来说，每个层都有批量归一化，激活层则是ReLU6。 但是，projection layer的输出没有应用激活功能。作者发现，在该层之后使用非线性激活，实际上会破坏低维数据中有用的信息。

这样，MobileNet V2将连续包含17个这样的block，然后是规则的1×1卷积、全局平均池化层和分类层。 

> 注意：第一个block稍有不同，它使用具有32个通道的常规3×3卷积代替扩展层。

具体架构也可见下表。$t$是扩展因子，$c$是输出通道数，$n$是block的重复次数，$s$是步长，depthwise convolution的卷积核大小均为3 x 3。

|     Input      |   Operator    | $t$  | $c$  | $n$  | $s$  |
| :------------: | :-----------: | :--: | :--: | :--: | :--: |
| 224 x 224 x 3  |    conv2d     |  -   |  32  |  1   |  2   |
| 112 x 112 x 32 |  bottleneck   |  1   |  16  |  1   |  1   |
| 112 x 112 x 16 |  bottleneck   |  6   |  24  |  2   |  2   |
|  56 x 56 x 24  |  bottleneck   |  6   |  32  |  3   |  2   |
|  28 x 28 x 32  |  bottleneck   |  6   |  64  |  4   |  2   |
|  14 x 14 x 64  |  bottleneck   |  6   |  96  |  3   |  1   |
|  14 x 14 x 96  |  bottleneck   |  6   | 160  |  3   |  2   |
|  7 x 7 x 160   |  bottleneck   |  6   | 320  |  1   |  1   |
|  7 x 7 x 320   | conv2d 1 x 1  |  -   | 1280 |  1   |  1   |
|  7 x 7 x 1280  | avgpool 7 x 7 |  -   |  -   |  1   |  -   |
|  1 x 1 x 1280  | conv2d 1 x 1  |  -   |  k   |  -   |  -   |

# 二、V2的改进意义

 V2体系结构的主要变化是残差连接和扩展/投影层。

对于这种模型，通道数随时间增加，空间尺寸也会相应减少。 但总体而言，由于构成块之间连接的瓶颈层，张量保持相对较小，。如图3所示，我们可以看到数据流经V2网络的情况。

<p align="center">
    <img src = "https://machinethink.net/images/mobilenet-v2/LowDimensionality@2x.png" height="60pix">
    图3（源自Ref [2]）
</p>

相比之下，V1就使其张量变得更大（最大为7×7×1024）。

使用低维张量是减少计算量的关键。 毕竟，张量越小，卷积层要做的乘法就越少。

但是，仅使用低维张量并不能获得很好的效果！

因为应用卷积层过滤低维张量将无法提取大量信息。 考虑到这个因素，作者首先使用了expansion layer，得到大张量，s使用depthwise convolution对数据进行过滤；然后使用projection layer减小张量。可以说在这方面， MobileNet V2的模块设计做到了两全其美。

> 举例如图4所示，将块之间流动的低维数据视为真实数据的压缩包。Expansion layer充当解压缩器，它首先将数据还原为完整格式，然后depthwise layer执行重要的滤波工作，最后projection layer将数据压缩以使其再次变小 。

<p align="center">
    <img src = "https://machinethink.net/images/mobilenet-v2/Compression@2x.png" width = "550pix">
    图4（源自Ref [2]）
</p>



通过学习扩展层和投影层的参数，模型能够在网络的每个阶段最佳地（解）压缩数据。

至此，我们也就能理解，为什么作者将文中的残差连接方式称为“inverted residuals”，我们可以比较一下normal和inverted残差块的区别，如图5所示。

<p align="center">
    <img src = "https://i.loli.net/2020/09/28/bpWVlH6UPNLCv4E.png" width = "500pix">
    图5（源自Ref [1]）
</p>



 图5中，使用阴影线标记的block后面没有非线性层，通过每个block的宽度来表示相对通道数量。

# 三、V2与V1的效果比较

## 3.1 参数量和计算量

我们首先从学习的参数和所需的计算量开始，比较MobileNet V1和V2模型的大小。

| 版本        | MACs(millions) | Parameters(millions) |
| ----------- | -------------- | -------------------- |
| MobileNetV1 | 569            | 4.24                 |
| MobileNetV2 | 300            | 3.47                 |

数据来源于[V1](https://github.com/tensorflow/models/blob/master/research/slim/nets/mobilenet_v1.md)和[V2](https://github.com/tensorflow/models/tree/master/research/slim/nets/mobilenet)，它们采用的width multiplier均为1.0，数据越小代表效果越好。

MACs是乘法累加运算，这可测量对单张224×224 RGB图像进行推理所需的计算量。图像越大，需要的MAC越多。

仅从MAC数量来看，V2的速度应该几乎是V1的两倍。 但是，这不仅仅涉及计算数量。 在移动设备上，内存访问比计算慢得多。 不过，这里V2也有优势：它的参数量只有V1的80％。

## 3.2 准确率

接下来是准确率的比较。

| 版本        | Top-1 Accuracy | Top-5 Accuracy |
| ----------- | -------------- | -------------- |
| MobileNetV1 | 70.9           | 89.9           |
| MobileNetV2 | 71.8           | 91.0           |

这里的Top-1 Accuracy和Top-5 Accuracy是在[ImageNet](http://www.image-net.org/challenges/LSVRC/2012/)上获得的，[源代码](https://github.com/tensorflow/models/tree/master/research/slim/nets/mobilenet)作者声称结果来自与测试集，但查看代码后，结果似乎是从50,000张图像的验证集上获得的。

其实，比较模型之间的准确度可能会产生误导，因为我们需要准确了解模型的评估方式。 为了获得上述数字，将图像的中心区域裁剪到包含原始图像的87.5％的区域，然后将该裁剪的大小调整为224×224像素。

## 3.2 语义分割的效果

为了验证V1和V2在语义分割方面的能力，作者选用了PASCAL VOC 2012 dataset用来验证，（1）V1和V2分别作为DeepLabv3的特征提取器，（2）简化了DeepLabv3训练头，来加快计算，（3）使用了不同的推理策略来优化运行效果。验证的结果如下表所示。

| Network      | OS   | ASPP | MF   | Miou      | Params    | Madds     |
| ------------ | ---- | ---- | ---- | --------- | --------- | --------- |
| MobIleNet V1 | 16   | √    | ×    | 75.29     | 11.15M    | 14.25B    |
| MobIleNet V1 | 8    | √    | √    | 78.56     | 11.15M    | 941.9B    |
| MobIleNet V2 | 16   | √    | ×    | 75.7      | 4.52M     | 5.8B      |
| MobIleNet V2 | 8    | √    | √    | 78.42     | 4.52M     | 387B      |
| MobIleNet V2 | 16   | ×    | ×    | **75.32** | **2.11M** | **2.75B** |
| MobIleNet V2 | 8    | ×    | √    | 77.33     | 2.11M     | 152.6B    |
| ResNet-101   | 16   | √    | ×    | 80.49     | 58.16M    | 81.0B     |
| ResNet-101   | 8    | √    | √    | 82.7      | 58.16M    | 4870.6B   |

我们能够得到以下分析结果：

（1）某些推理策略，比如多尺度输入、增加左右翻转的图像，会极大增加乘法累加量，因此不适合于移动设备的应用；

（2）使用output stride = 16的效率要比output stride = 8的效率高；

（3）MobileNetV1已经是强大的功能提取器，其所需的乘法累加量比ResNet-101 少4.9-5.7倍；

（4）在MobileNetV2的倒数第二个特征图后构建DeepLabv3训练头的效率更高，因为倒数第二个特征图包含320个通道，而不是1280个。因此，在获得类似性能的情况下，但是MobileNetV2所需的运算量比MobileNetV1少2.5倍。

（5）DeepLabv3原先的训练头十分消耗计算力，若删除ASPP模块能够显著降低计算量，但性能只会略微下降。

# Reference

[1]. [MobileNetV2: Inverted Residuals and Linear Bottlenecks](https://arxiv.org/abs/1801.04381)

[2]. [MobileNet version 2](https://machinethink.net/blog/mobilenet-v2/)