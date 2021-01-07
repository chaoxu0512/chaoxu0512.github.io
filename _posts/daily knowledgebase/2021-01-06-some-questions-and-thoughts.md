---
layout:     post
title:      今日疑问和知识
subtitle:   
date:       2021-01-06
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Daily Knowledgebase
---

**1.为什么在OCT系统中，各种光纤均采用了FC/APC的接口，而非FC/PC呢？DC/APC接口的优势在哪里？**

[这里](https://www.vialite.com/resources/guides/apc-vs-pc-connectors/)比较详细解答了这个问题。其核心就在于APC的端面和光纤纵向主要有8度的斜角，减小了反向噪声的影响；PC的端面和光纤纵向完全垂直。

**2.在测量某一个fiber adaptor的insertion loss时，其一侧的光纤连接光源，另一测连接光谱分析仪。在连接处，使用不同的旋紧程度会得到不同的输出功率。通常在光纤插入fiber adaptor后，旋钮旋得越紧，记录得到的输出功率会越小。为何？（测试fiber adaptor为SWIKOH GIKEN SAA-4，光源端的光纤为HI 780，测量端的光纤为780HP）**

今天，我使用了另一个fiber adaptor为ADAFC3，此时的情况是：旋钮越紧，输出的功率值越大。之前，我以为是旋钮越松，会有外界的光漏到光纤里；现在看来并不是这样。我推断，出现这种情况，应该与fiber adaptor、fiber connector以及光谱仪处optical input的接口形状参数有关。

在使用ADAFC3型号的adaptor时，还有一个情况，也是和设备的接口参数有关。如下图1，我首先测量L处fiber connector的输出功率$P_1$，然后连接好L connector、fiber adaptor和O connector，测得功率为$P_2$，结果$P_1$<$P_2$。注意到，每次测量功率的时候，我都是将对应的fiber connector连接到光谱仪的optical input。出现这种情况，很有可能就是因为两种connector与optical input存在不同的接触效果。

<p align="center">
<img src="https://i.loli.net/2021/01/07/fxjOy1h2voeJNm4.jpg" width=400pix>
</p>
<p style="text-align:center;">图1. L connector、fiber adaptor和O connector.</p>

<p align="center">
<img src="https://i.loli.net/2021/01/07/WlgsQeIjC8RcGvN.jpg" width=400pix>
</p>
<p style="text-align:center;">图2.光谱仪的optical input.</p>

另外一个因素，我提一下，虽然应该与这个情况无关。L connector连接的光纤是HI 780，O connector连接的光纤是780HP，两者Core NA和Core diameter有些差别。

最后的最后，还有一个可能，那就是测量的偶然性。

**3.今天导师提到，在系统中若使用了780HP的光纤，则其他光纤组件均应为780HP，为何？**

这个问题其实很简单，在一个OCT系统中，如果reference arm和sample arm的光纤不一样，那么对应的群速度色散曲线也将不相同，这无疑增加了补偿难度。