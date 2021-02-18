---
layout:     post
title:      在OCT系统的reference arm中加入prism pair时出现的问题
subtitle:   
date:       2021-02-18
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Daily Knowledgebase
---

在OCT的reference arm中加入棱镜对，主要是为了补偿sample arm中的色散。

首先做的就是在基座上固定棱镜，采用的胶水是[G14250](https://www.thorlabs.com/thorproduct.cfm?partnumber=G14250)。在粘的时候，我考虑到了要让棱镜的斜面略突出于基座，这样可以缓解两个斜面不平行的问题（可以轻转下图中右边的基座）。但是，我忽略了一个问题，在垂直方向上，棱镜底面的胶水没有混匀，导致棱镜不水平，可以看到下图中俩棱镜仅靠，但却不能完全贴合（可能是在胶水凝固过程中，温度变化引起的底面胶水不均匀）。

其次，就是右边基座的松紧与固定的问题。左边的基座需要完全固定，而且棱镜斜面需尽量与其linear stage的运动方向平行。一般，为了缓解两个棱镜斜面不完全平行的问题，右边的基座不能完全锁紧，这样，在linear stage前后移动改变光程差的时候，右边的棱镜能做出相应的移动。如果右边基座过紧，并且左右棱镜斜面不完全平行，在移动过程中，就会可能出现压力过大，使棱镜边缘损坏（图中左边棱镜的右上角）。但是，我的这个设计中，当右边基座较松时，它不仅会做旋转运动，还会出现水平偏移。后者是我不想要的，这也是我设计时欠考虑的。目前能想到的补救措施，就是切一块铝板，钻一个M6的孔，粘在右边基座的轴向位置。这样能够限制基座的水平偏移。不过这一步，需要在最后确定位置以后才能实施，现在我还在不断调试位置。

<img src="http://imghost.cx0512.com/images/2021/02/18/20210218213723.jpg" alt="prism pair in rederence arm" style="zoom: 50%;" />

下一步，就是在两块棱镜之间加油了。目前还没做，也会有不少坑。因为我用的玻璃是SF11，室温下折射率大概是1.76，所以用的油越接近这个折射率越好了。现在我能找到的是1.56的油。之前有人推荐用[Cytoseal 60](https://www.fishersci.com/shop/products/richard-allan-scientific-cytoseal-60-280/p-4532396)，说挺好的，但手上没货。