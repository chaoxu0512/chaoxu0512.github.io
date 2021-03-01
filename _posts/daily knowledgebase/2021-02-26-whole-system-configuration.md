---
layout:     post
title:      OCT系统中的整体思考
subtitle:   
date:       2021-02-26
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Daily Knowledgebase
---
如导师所说的，做事要提前布局，思考接下来几周甚至几个月将要做的事情，先想好了再动手。这种事情，要是自己不踩坑，很难有深刻体会的。今天，我就花了将近一天的时间，用来考虑接下来几个月的工作，既包括general的器件，也有specific的实验操作。当然，我的进度必然是比较慢的。

对于一个OCT系统，它有四条臂，今天考虑了它的光源臂和参考臂。首先是光源这一侧。对于一个800nm的系统，我们目前已经有了光源[Broadlighter-M](https://www.superlumdiodes.com/brl-m-dtq-series.htm)，它的中心波长大约是842nm，带宽约为160nm，经过测试，其波形较为平坦。但是对于560nm的系统，我们采用的光源是[SuperK EXW-6](https://www.nktphotonics.com/lasers-fibers/product/superk-extreme-fianium-supercontinuum-lasers/)，但是需要对这个光源的光谱进行截断，就需要一个spectral filter，这里采用[SuperK SPLIT spectral filter](https://www.nktphotonics.com/lasers-fibers/product/superk-split-spectral-supercontinuum-splitter/)。关于这个spectral filter，它有两种工作模式，分别是VIS/IR和nIR/IR，在我们的应用中，我们将会选择前一种工作模式。

<p align="center">
<img src="https://www.nktphotonics.com/wp-content/uploads/sites/3/2015/02/split-performance-summary-vis.jpg" width=600pix>
</p>
<p style="text-align:center;">Split performance summary vis.</p>

这个filter还需要与[SuperK CONNECT](https://www.nktphotonics.com/lasers-fibers/product/superk-connect-broadband-fiber-delivery/)相连，最后再与FC/APC的2mm narrow key的fiber connector相连接。

目前，我们已经订购了460HP、780HP和SMF28e的fiber patchcord，都是FC/APC接口的。

接下来，将这个fiber connector，分别连接light source arm 和fiber coupler。目前我们有的是50:50的型号 [TW850R5A2](https://www.thorlabs.com/thorproduct.cfm?partnumber=TW850R5A2)，**需要考虑的是，能否选择70:30或者90:10的呢**？

fiber coupler输出的一路就是reference arm。在到达collimator以前，可以添加一个polarization controller，目前采用[FPC025](https://www.thorlabs.com/thorproduct.cfm?partnumber=FPC025)，**需要思考的是，它的作用以及使用方法**。它不需要额外的辅助器件，但是会对光纤的长度有一定要求。

再往下，就需要collimator，目前使用的是[TC18APC-850](https://www.thorlabs.com/thorproduct.cfm?partnumber=TC18APC-850)，针对850nm激光进行优化的透射式准直镜，采用的配件有AD12BA和KS05K_M。接下来我们会考虑使用[RC08APC-P01](https://www.thorlabs.com/thorproduct.cfm?partnumber=RC08APC-P01)，减少光束通过透射式光学元件的损失和可能的色散。**Consider why we choose this model**. 对于这个反射准直镜， [SPW909](https://www.thorlabs.com/thorproduct.cfm?partnumber=SPW909) Spanner Wrench，我们还需要对应的adjustable holder，采用的是[POLARIS-K1](https://www.thorlabs.com/thorproduct.cfm?partnumber=POLARIS-K1)。这个holder采用的post是M4沉头孔。

接着，光束从reflective collimator出来以后，会通过一个prism pair，我们采用的是Edmund的[N-SF11 uncoated 15mm right angle prisms](https://www.edmundoptics.com/f/n-sf11-right-angle-prisms/12466/)，使用折射率更高的玻璃可以增大光程差，从而减小整个reference arm的长度。 之所以不采用coated prism，是因为在我们的应用中，我们希望光顺利通过棱镜对的直角面。不过，我们现在还在国内寻找合适的生产商，降低成本，缩短供应时间。**这里有一个关键就是prism的holder，这是需要自己设计的**。我们使两个prism的hypotenuse surface<u>尽量贴合</u>， 固定一个prism，然后使用linear translational stage控制另一个prism沿着斜面前后移动，改变光程。这里需要精确控制prism的水平和贴合，就对holder提出了很高的要求。另外，用胶水粘prism时，也需要特别注意其底部的平行。要是粘错了，可以用Acetone浸泡24小时，清除胶水。在hypotenuse surface之间加油的注意事项，前文已经提到了。

之后，我们还需要一个[NDC-50C-4M-A](https://www.thorlabs.com/thorproduct.cfm?partnumber=NDC-50C-4M-A)控制reference arm的光强度。最后，使用的反射镜为protected silver 的[PF05-03-P01](https://www.thorlabs.com/thorproduct.cfm?partnumber=PF05-03-P01)。这里有一个点，**mirror应该放在哪个位置，才最有利于coupling efficiency的最大化**；另外，**为什么选择镀银的反射镜，而不是镀金或镀铝**。

然后，需要考虑的就是sample arm。经过FC/APC的fiber connector以后，对于endoscopic OCT，我们需要的一个探针，其关键就是rotary joint（[Endoscopic optical coherence tomography: technologies and clinical applications](http://dx.doi.org/10.1364/boe.8.002405)）；对于ophthalmological OCT，首先，我需要知道galvo system是如何工作的。

