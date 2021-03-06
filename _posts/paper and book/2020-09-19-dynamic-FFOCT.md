---
layout:     post
title:      理解 Dynamic full-field optical coherence tomography
subtitle:   视网膜细胞器的3D活体成像
date:       2020-09-19
author:     Chao Xu
header-style: text
hidden: false
mathjax: false 
catalog: true
tags:
    - Paper and Book
    - Optical Coherence Tomography
---

原文来自于：[Dynamic full-field optical coherence tomography: 3D live-imaging of retinal organoids](https://www.nature.com/articles/s41377-020-00375-8)。

# 一、背景

1. 对3D生物结构成像存在诸多挑战，比如：生物结构相对来说透明，若不对其染色，很难获得高对比度；3D生物结构具有一定的厚度，在使用光学成像仪器时要注意对焦和离焦位置。
2. 在对human induced pluripotent stem cells (hiPSCs)诱生的视网膜细胞器成像时，传统方法存在缺陷，包括：需要固定或机械切片；需要标记；缺乏功能对比。
3. OCT能很好地对生物组织进行3D成像，反向散射地特性提供了较强的对比度。它的缺陷在于成像深度和分辨率之间存在矛盾，比如：增加lateral resolution，就需要增大NA，但是这样会减小depth of  field，导致只有一小层能清楚成像。
4. Time domain full-field OCT (FFOCT)的特点：相比于传统的OCT en face图像，在en face平面具有更高的空间和时间分辨率，在增大NA的同时不必牺牲成像深度 。

在以上的情况下，作者提出了dynamic FFOCT((D-FFOCT)，能够测量反向散射光的时间波动 。在极弱的反向散射光时，基于local intra-cellular motility，依旧能获得较好的对比度、亚微米空间分辨率、毫秒级的时间分辨率。

D-FFOCT的影响：

1. D-FFOCT imaging creates a new label-free non-invasive contrast for imaging retinal organoids. 
2. D-FFOCT allows imaging of different layers at multiple depths while preserving the sample integrity。

# 二、正文

摘要：光学相干断层成像(OCT)能够对活体组织的复杂结构进行成像，但是缺少功能性信息。文中提出了一种动态全场的OCT技术，非侵入性地对多功能干细胞诱生的视网膜细胞器进行活体成像。研究中生成了的彩色图像具有内生性对比度，它与细胞器的运动性有关。此外，这些 图像的空间分辨率达到了亚微米级别，时间分辨率则达到了毫秒级别。这样，在活体组织中，研究人员就能根据细胞的功能对细胞进行分类。

**图1. 实验装置和图像后处理。图像的获取。尺度条：50um。**

<p align="center"><img src="https://imghost.cx0512.com/images/2020/09/19/v2-32dc060717da369c5d917830ed0783fc_b.png" alt="v2-32dc060717da369c5d917830ed0783fc_b.png" border="0" />
</p>

**图1a.** 动态全场OCT装置和宽场荧光显微镜。PZT，压电跃变；TS，平移台；BPF，带通滤波器；HPF，高通滤波器；因为荧光分子和D-FFOCT都是在相同的光谱范围内进行记录，所以无法对两者同时成像。在这种情况下，实验装置中增加了一个flip mirror，用于成像模式的转换。

**图1b.** 处理前获得的3D立方体数据(x, y, t)。每个时间单位下，每个像素都是单独处理的。

**图1c.** 在活体视网膜细胞器内，对一个像素的强度进行持续绘制。

**后处理步骤：图1d-图1f，在HSV颜色空间中计算动态图像。**

**图1d.** 根据平均频率计算色度(Hue)，从蓝色(低时间频率)到红色(高时间频率)。

**图1e.** 饱和度(Saturation)是频率带宽的倒数。结果，具有更宽的带宽的信号(白噪声)会显得颜色单调，但窄带宽的信号就会显得颜色丰富。

**图1f.** 纯度(Value)是运行标准差。基准是D29视网膜细胞器。

**图1g.** 平均频率的计算结果(色度)。

**图1h.** 频率带宽的计算结果(饱和度)。

**图1i.**  动态结果(纯度)。

**图1j.** 重建结果。

**图2. 使用D-FFOCT对hiPSC诱生的视网膜细胞器进行成像。尺度条：20um。**

<p align="center"><img src="https://imghost.cx0512.com/images/2020/09/19/v2-84945582b579045ea54c133a3738810b_b.png" alt="v2-84945582b579045ea54c133a3738810b_b.png" border="0" />
</p>

**图2a.** 球状D28视网膜细胞器的3D重建结果，包含了直径约5um的细胞。红色箭头指的地方，是表面细胞，具有高动态性。

**图2b.** 展示的是**图2a**蓝色方框中的某一块。

**图2c.** 展示的是图2a绿色虚线处的横截面，可以看到视网膜细胞器中各层的组织。

<p align="center"><img src="https://imghost.cx0512.com/images/2020/09/19/v2-320917dccffe4ef336f9ee69e743440c_b.png" alt="v2-320917dccffe4ef336f9ee69e743440c_b.png" border="0" />
</p>

**图2d.** 在3小时内，定时对细胞器的两个区域进行成像。第一行的放大图像显示了两个区域的动态变化，这能够反映出一个差分的过程，其中红色的虚线是两个区域的分界线。第二行的图像则显示了另一个非常活跃的区域（其余细胞器的中央），包含了某些快速、高动态的细胞，它们可能正在经历细胞凋亡。

**图2e.** 对于**图2a-图2d**的3D和定时成像D-FFOCT图，都采用相同的颜色条。在一个D147视网膜细胞器上进行了高时间辨率的成像。

<p align="center">
    <img src="https://imghost.cx0512.com/images/2020/09/19/v2-46fef939bd345a6bd7c5c20c1cabcd95_b.png" alt="v2-46fef939bd345a6bd7c5c20c1cabcd95_b.png" border="0" />
</p>

**图2f.** 视网膜细胞器的一部分，在这里展现为梭形结构，对应于光感受器外段(photoreceptor outer segments)。

**图2g.** 在三种不同状态下，细胞核的放大视图。(i)正常状态下的细胞核，紧凑、形状均匀、很明亮(表示有强活动性)；(ii)一个垂死的、膨胀的细胞核，几乎没有细胞活动性；(iii)正在进行分裂的细胞核，细胞质(cytoplasm)中没有明确的核膜，细胞核的两个不同部分(白色箭头)(表明细胞核有丝分裂(mitosis)，染色体(chromosomes)已经分裂，与正常细胞核具有相同的亚细胞活性)。

**图2h.** 类似于光感受器外段的结构的放大图(从侧面成像)；其中三个用白线标记。

**图3. D-FFOCT成像的荧光验证。D-FFOCT图像以彩色在图3(b-d, f)中展示。覆盖宽场荧光图像的D-FFOCT图像以灰度(D-FFOCT)和红色(荧光)表示(a, e)。尺度条：(a-d)10um；(e, f)50um。**

<p align="center">
   <img src="https://imghost.cx0512.com/images/2020/09/19/v2-2de745f2b10a834a78a3c9459a6393e0_b.png" alt="v2-2de745f2b10a834a78a3c9459a6393e0_b.png" border="0" />
</p>

**图3a-图3d.** D29视网膜使用燃料进行标记，目标是死细胞的细胞核。

**图3a.** 可以看到两个死细胞，这里用两个红点标记，与**图3b**中的两个暗区域相对应。在D-FFOCT图像中这两个区域没有显示任何动态信号。

**图3c-图3d.** 两个暗区域的放大图像(用白色虚线表示，对应于应光成像的两个红点)。

<p align="center">
<img src="https://imghost.cx0512.com/images/2020/09/19/v2-8cd3fb1ba8d20e120b9cdb13a7c7f2ad_b.png" alt="v2-8cd3fb1ba8d20e120b9cdb13a7c7f2ad_b.png" border="0" />
</p>

**图3e.** 在荧光图像上的某些光感受器与**图3f**的某些细胞(用蓝色和绿色表示)相匹配，这些区域在白色虚线范围内。这些光感受器的前体细胞有其独特的动态特征，可以仅用D-FFOCT图像将其与周围的细胞区分开来。

# 三、方法

## **1. Human iPSC maintenance and retinal differentiation**

这一步主要是培养人体iPSC，视网膜分离，然后提取视网膜细胞器。

## **2. Sample preparation for D-FFOCT imaging**

这里主要提到了对样品成像前的保存以及成像后的处理。样品(视网膜细胞器)放在sample arm，通过三轴位移台控制它的运动。

## **3. Immunostaining and imaging of retinal sections**

Immunostaining指的是免疫染色， 这里主要用到了一种叫phosphate- buffered saline的溶液。样品制成切片后，然后还用了各种抗体。

关于切片的成像：Fluorescent staining signals were captured with an Olympus FV1000 confocal microscope.

## **4. Experimental setup**

做完前期工作以后，终于来到了关键部分。

这里先回顾一下T-FFOCT，它使用高精度电机在轴向进行扫描，获得3D图像；再加上使用了宽带LED作为光源，这样就提供了更高的轴向(axial)和正面(en face)分辨率。同时，T-FFOCT还可以对体外的组织样品进行成像。 

文中使用的D-FFOCT，用于对视网膜细胞器进行成像。它的横向分辨率为0.5um(使用高倍率的水浸物镜，40x 0.8NA)，视场为~320x320(um^2)。受益于较高的NA，其纵向分辨率也达到了1.7um。在这里，

对于D-FFOCT的光源选择：中心波长为660nm的LED，**光源的相干长度(即纵向相干条纹的FWHM)比焦深更大**。有几点需要考虑的：

(1) spatially incoherent to avoid cross-talk artefacts due to multiple scattering. 

(2) The optical power must be high enough to image close to camera saturation to maximize the signal-to-noise ratio.

(3) 光源的中心波长既要靠近NIR(增加穿透深度)，又要在VIS(荧光成像在VIS；有些光学元件在VIS镀膜)

(4) **光源的相干长度在水中是13.28um，促进了相干平面和焦平面的对准，进而在整个视场范围内获得均匀的对比度。**

为了验证，实验中还加入了荧光显微成像，其LED光源的中心波长为565nm，用作激发光源；然后使用带通滤波器，得到的中心波长为562nm、带宽为40nm的光束。然后再经过一个中心波长为624nm的带通滤波器，最后在荧光sCMOS相机上成像(见图**1a**)。

# 四、Reference

[1]. [Dynamic full-field optical coherence tomography: 3D live-imaging of retinal organoids](https://www.nature.com/articles/s41377-020-00375-8)

[2]. [关于FFOCT，具体请见原文](https://www.osapublishing.org/ao/abstract.cfm?uri=ao-43-1)

[3]. [关于D-FFOCT，具体请见原文](https://www.osapublishing.org/boe/abstract.cfm?uri=boe-7-4-1511)