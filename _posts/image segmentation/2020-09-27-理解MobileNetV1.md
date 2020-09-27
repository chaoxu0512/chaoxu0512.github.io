---
layout:     post
title:      理解MobileNetV1
subtitle:   
date:       2020-09-27
author:     Chao Xu
header-img: img/606216.jpg
catalog: true
tags:
    - Image Segmentation
---

在本文中，主要介绍了[MobileNetV1](https://arxiv.org/abs/1704.04861)，其中使用的深度可分离卷积能够减小模型尺寸和复杂度，这对于移动端和嵌入式的视觉应用十分有效。作者提出了两个全局超参数（宽度乘子和分辨率乘子），用于取得效率和准确率之间的平衡。MobileNetV1的核心就是更小、更高效。

# 一、深度可分离卷积

深度可分离卷积之所以如此命名，是因为它不仅涉及空间维度，而且涉及深度维度（通道数）。深度可分离卷积将一个内核拆分为两个独立的内核，这些内核执行两个卷积：逐深度卷积（depthwise convolution）和逐点卷积（pointwise convolution）。 但首先，让我们看看普通卷积的工作原理。

## 1.1 普通卷积

一般来说，典型的图像不一定是2D图像， 它可能具有深度、宽度和高度。 我们假设有一张12 x 12 x 3像素的输入图像。我们在图像上进行5 x 5的卷积，不使用填充，步幅为1。如果仅考虑图像的宽度和高度，则卷积过程类似于：12 x 12$ \to $5 x 5$ \to $ 8 x 8。 在5x5内核中，每25个像素进行标量乘法，每次给出1个数字。 由于没有填充(12 - 5 + 1 = 8)，因此最终得到8x8像素的图像。

但是，由于图像具有3个通道，因此我们的卷积内核也需要具有3个通道。 这意味着，每次内核移动时，我们实际上都执行5 x 5 x 3 = 75乘法，而不是执行5 x 5 = 25乘法。

如图1所示，我们以每25个像素执行标量矩阵乘法，输出1个数字。 经过5 x 5 x 3内核后，12 x 12 x 3图像将变为8 x 8 x 1图像。

<p align="center">
  <img src="https://i.loli.net/2020/09/27/wRBQDTzelP25rVq.png" title="一个普通卷积，其输出为8 x 8 x 1">
    图1. 一个普通卷积，其输出为8 x 8 x 1（源自：Ref [2]）
</p>


如果我们想增加输出图像中的通道数怎么办？ 如果我们想要大小为8 x 8 x 256的输出怎么办？如图2所示，我们可以创建256个内核来生成256张8 x 8 x 1图像，然后将它们堆叠在一起以创建8 x 8 x 256图像输出。

<p align="center">
  <img src="https://i.loli.net/2020/09/27/Jlm8hevDo1syUxP.png" title="一个普通卷积，其输出为8 x 8 x 256">
    图2. 一个普通卷积，其输出为8 x 8 x 256（源自：Ref [2]）
</p>


这就是普通卷积的工作方式。 可以将其视为一个函数：12 x 12 x 3 $ \to $ 5 x 5 x 3 x 256$ \to $12 x 12 x 256（其中5 x 5 x 3 x 256表示内核的高度、宽度、输入通道数和输出通道数）。我们不是将整个图像乘以内核，而是将内核移动到图像的每个部分，并分别乘以一小部分。

## 1.2 逐深度卷积

在第一部分的逐深度卷积中，我们在不改变深度的情况下为输入图像进行了卷积。 如图3所示，我们通过使用3个形状为5x5x1的内核来实现。

<p align="center">
  <img src="https://i.loli.net/2020/09/27/qVjwFlpZrxKGNui.gif" title="在一幅三通道图像中迭代三个卷积核">
    图3. 在一幅三通道图像中迭代三个卷积核（源自：Ref [2]）
</p>


如图4所示，每个5 x 5 x 1内核都会迭代图像的1个通道（注意：1个通道，而不是所有通道），获得每25个像素组的标量积，从而给出8 x 8 x 1图像。 将这些图像堆叠在一起将创建一个8 x 8 x 3的图像。

<p align="center">
  <img src="https://i.loli.net/2020/09/27/3DThtBQzRipEkey.png" title="逐深度卷积，使用3个卷积核将一幅12 x 12 x 3图像转化为8 x 8 x 3图像">
    图4. 逐深度卷积，使用3个卷积核将一幅12 x 12 x 3图像转化为8 x 8 x 3图像（源自：Ref [2]）
</p>


## 1.3 逐点卷积

原始的普通卷积将12 x 12 x 3图像转换为8 x 8 x 256图像。 当前，深度卷积已将12 x 12 x 3图像转换为8 x 8 x 3图像。 现在，我们需要增加每个图像的通道数。

逐点卷积之所以如此命名，是因为它使用了1 x 1的内核或迭代遍历每个点的内核。 该内核的深度为输入图像所具有的通道数。 因此，如图6所示，我们将1 x 1 x 3内核在8 x 8 x 3图像上进行迭代，以获得1张8 x 8 x 1的图像。

<p align="center">
  <img src="https://i.loli.net/2020/09/27/hrJQzdglqoW4mB6.png" title="逐点卷积，将一幅8 x 8 x 3图像转化为8 x 8 x 1图像">
    图5. 逐点卷积，将一幅8 x 8 x 3图像转化为8 x 8 x 1图像（源自：Ref [2]）
</p>


如图6所示，我们可以创建256个1 x 1 x 3内核，每个内核输出8 x 8 x 1图像，以得到形状为8 x 8 x 256的最终图像。

<p align="center">
  <img src="https://i.loli.net/2020/09/27/GNWpJ4cbsoSUn59.png" title="逐点卷积，使用256个卷积核将一幅8x8x3图像转化为8x8x256图像">
    图6. 逐点卷积，使用256个卷积核将一幅8x8x3图像转化为8x8x256图像（源自：Ref [2]）
</p>


我们将卷积分为：深度卷积和点卷积。如果原始的普通卷积为12 x 12 x 3$ \to $5 x 5 x 3 x 256$ \to $8 x 8 x 256，我们可以将这种新卷积说明为12 x 12 x 3$ \to $5 x 5 x 1 x 3$ \to $1 x 1 x 3 x 256$ \to $8 x 8 x 256。

## 1.4 深度可分离卷积的优势

我们计算一下在普通卷积中执行的乘法次数，有256个5 x 5 x 3内核，可移动8 x 8次，那就是256 x 3 x 5 x 5 x 8 x 8 = 1,228,800乘法。

深度可分离卷积呢？在逐深度卷积中，我们有3个5 x 5 x 1内核，它们移动了8 x 8次。那就是3 x 5 x 5 x 8 x 8 = 4,800次乘法。在逐点卷积中，我们有256个1 x 1 x 3内核，它们移动8 x 8次。那就是256 x 1 x 1 x 3 x 8 x 8 = 49,152次乘法。 最后，将它们加在一起，就是53,952次乘法。

52,952比1,228,800少得多。 通过较少的计算，网络可以在更短的时间内处理更多内容。但是，这两个网络是在做同样的事情么？在这两种情况下，我们都将图像通过5 x 5内核，将其缩小到一个通道，然后将其扩展到256个通道。 为什么一个为什么比另一个快两倍以上呢？

**主要区别在于：在正常卷积中，我们将图像变换了256次。 并且每个变换都使用5 x 5 x 3 x 8 x 8 = 4800次乘法。 在深度可分离卷积中，我们只对图像进行1次真正的变换-即在逐深度卷积。然后，我们获取转换后的图像并将其简单地拉长到256个通道。 无需一遍又一遍地变换图像，这样我们就可以节省计算能力。**

# 二、网络架构

MobileNetV1的网络架构如下图7所示。

<p align="center">
  <img src="https://i.loli.net/2020/09/27/XkSqEvZRwOU9ngr.png" title="MobileNetV1的网络架构">
    图7. MobileNetV1的网络架构（源自：Ref [1]）
</p>


MobileNet就是建立在深度可分离卷积上的，但是它的第一层是完全卷积层。除了最后的全连接层（无需非线性，连接softmax用于分类），所有卷积层（包括深度可分离卷积）后均添加了BN层和ReLU层，如下图8所示。在第一层和深度可分离卷积中，均采用了跨步卷积来进行下采样。此外，在全连接层之前，作者使用了一个平均池化层，将空间分辨率降为1。若将逐深度卷积和逐点卷积归为单独的层，那么MobileNet一共有28层。

 <p align="center">
  <img src="https://i.loli.net/2020/09/27/YhANWsbmnFqta7z.png" title="普通卷积（左），带有BN和ReLU的深度可分离卷积（右）">
    图8. 普通卷积（左），带有BN和ReLU的深度可分离卷积（右）（源自：Ref [1]）
</p>


# 三、宽度乘子$\alpha $

作者在网络中引入了宽度乘子$\alpha $，主要是为了控制某一层的输入宽度。原文中提到：

> The role of the width multiplier α is to thin a network uniformly at each layer.

通常，我们可以将$\alpha $设置为1、0.75、0.5和0.25。当$\alpha = 1$时，我们得到的就是基础的MobileNet。对于给定的一个层和宽度乘子$\alpha $，输入通道数就会从$M$变成$\alpha M$，输出通道数就会从$N$变成$\alpha N$。随着$\alpha $的减小，计算损耗和参数量呈二次函数下降的趋势。

> Width multiplier has the effect of reducing computational cost and the number of parameters quadratically by roughly $\alpha ^2$. 

| Width Multiplier   | ImageNet Accuracy | Million Mult-Adds | Million Parameters |
| ------------------ | ----------------- | ----------------- | ------------------ |
| 1.0 MobileNet-224  | 70.6%             | 569               | 4.2                |
| 0.75 MobileNet-224 | 68.4%             | 325               | 2.6                |
| 0.5 MobileNet-224  | 63.7%             | 149               | 1.3                |
| 0.25 MobileNet-224 | 50.6%             | 41                | 0.5                |

可以看到当$\alpha $从1.0降至0.5的过程中，准确率的下降都是十分平缓的。但是$\alpha$=0.25时，准确率下降较大，说明此时宽度乘子过小了。

# 四、分辨率乘子$\rho $

此外，作者还在网络中引入了分辨率乘子$\rho $，控制输入图像的分辨率。原文中提到：

> We apply this (resolution multiplier) to the input image and the internal representation of every layer is subsequently reduced by the same multiplier.

$\rho $的范围在0到1之间，初始输入图像的分辨率为224，这是基础的MobileNet。当$\rho $分别等于0.86,0.71,0.57时，输入图像的分辨率分别为192,160,128。不过，这里$\rho $的数值是通过改变分辨率来隐性设置的。此外，计算损耗会以$\rho ^2$的速度下降。

> Resolution multiplier has the effect of reducing computational cost by $\rho ^2$.

| Resolution Multiplier | ImageNet Accuracy | Million Mult-Adds | Million Parameters |
| --------------------- | ----------------- | ----------------- | ------------------ |
| 1.0 MobileNet-224     | 70.6%             | 569               | 4.2                |
| 1 MobileNet-192       | 69.1%             | 418               | 4.2                |
| 1 MobileNet-160       | 67.2%             | 290               | 4.2                |
| 1 MobileNet-128       | 64.4%             | 186               | 4.2                |

可以看到当分辨率从224降至128的过程中，准确率的下降都是十分平缓的。

# 五、其他结果

根据$\alpha  \in \{ 1,0.75,0.5,0.25\} $和$res \in \{ 224,192,160,128\} $，设计了16个模型，图9显示了ImageNet准确率和计算次数的关系，图中的结果是采用底数线性处理的。可以看到当$\alpha$=0.25时，准确率有一个跃升。图10 显示的是ImageNet准确率和参数量之间的关系。

 <p align="center">
  <img src="https://i.loli.net/2020/09/27/81mqjlyJLoNk9RX.png" title="ImageNet准确率和计算量之间的关系">
    图9. ImageNet准确率和计算量之间的关系（源自：Ref [1]）
</p>

 <p align="center">
  <img src="https://i.loli.net/2020/09/27/YPtMmzTf8KrWloU.png" title="ImageNet准确率和参数量之间的关系">
    图10. ImageNet准确率和参数量之间的关系（源自：Ref [1]）
</p>


# 六、应用

（1）更精细的识别

（2）大尺度的地理定位

（3）人脸识别

（4）目标检测

# 七、思考

为什么MobileNet能够加快网络训练速度呢？

首先就是使用了深度可分离卷积，这极大的减少了计算量（Mult-Adds）。但还有另一方面需要考虑的，那就是网络的实现方式。作者提到：

> Our model structure puts nearly all of the computation into dense 1×1 convolutions. This can be implemented with highly optimized general matrix 0.0multiply (GEMM) functions.
>
> 1×1 convolutions do not require initial reordering in memory and can be implemented directly with GEMM which is one of the most optimized numerical linear algebra algorithms.

然后作者给出了各个网络层的计算和参数占比，如下表所示。

| Type            | Mult-Adds | Parameters |
| --------------- | --------- | ---------- |
| Conv 1 x 1      | 96.86%    | 74.59%     |
| Conv DW 3 x 3   | 3.06%     | 1.06%      |
| Conv 3 x 3      | 1.19%     | 0.02%      |
| Fully Connected | 0.18%     | 24.33%     |

那什么是GEMM呢？其实它就是泛化矩阵-矩阵乘法。原文中提到的reordering的解释可以参照matlab中的函数`im2col`，也可以见下图的解释。

 <p align="center">
  <img src="https://i.loli.net/2020/09/27/F7jdByDeWRQkOzs.png" title="im2col的解释">
    图11. im2col的解释（源自：Ref [4]）
</p>


由此，我们就可以明白为什么作者说1 x 1卷积不需要reordering，因为这个卷积只有Patch 1。关于GEMM的由浅入深的解释，可见这里：[Why GEMM is at the heart of deep learning](https://petewarden.com/2015/04/20/why-gemm-is-at-the-heart-of-deep-learning/)。

接下来，回到原文中，作者还提到了另外两点。

> （1）使用更少的正则化和数据增强，因为小模型一般不需要担心过拟合的问题。
>
> （2）尽量减少对逐深度卷积使用权值下降，因为很明显，它们的参数已经够少了。

除此以外，作者还应用了MobileNet的核心超参数，也就是宽度乘子和分辨率乘子。

# Reference

[1]. [MobileNets: Efficient Convolutional Neural Networks for Mobile Vision Applications](https://arxiv.org/abs/1704.04861)

[2]. [A Basic Introduction to Separable Convolutions](https://towardsdatascience.com/a-basic-introduction-to-separable-convolutions-b99ec3102728)

[3]. [Review: MobileNetV1 — Depthwise Separable Convolution (Light Weight Model)](https://towardsdatascience.com/review-mobilenetv1-depthwise-separable-convolution-light-weight-model-a382df364b69)

[4]. [Why GEMM is at the heart of deep learning](https://petewarden.com/2015/04/20/why-gemm-is-at-the-heart-of-deep-learning/)