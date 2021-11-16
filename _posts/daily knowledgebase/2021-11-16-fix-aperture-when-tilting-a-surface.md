---
layout:     post
title:      Zemax中倾斜反射面时保持孔径不变的方法
subtitle:   
date:       2021-11-16
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - daily knowledgebase
    - zemax
---

问题描述：

I would like to simulate that light travels through a single mode fiber and a coreless fiber, and the end of the coreless fiber is a tilted flat surface, so the light will be reflected because of total internal reflection or reflective coating. My problem is that I can not keep the aperture constant (usually the cladding of SMF and my coreless fiber is 125um) because of the titled surface, as shown below. Is there any method that is able to keep the diameter consistent (125um) ? 

![image.png](https://i.loli.net/2021/11/16/pgKaIEB4jWhvntP.png)

![image.png](https://i.loli.net/2021/11/16/Ai46EmHzPsDaeq2.png)

解决方案：

I indeed find a method to keep the aperture constant (according to what I understand).

I can set the Aperture Type of Surface 3 as Elliptical Aperture, the X-Half Width is 0.0625 (just the radius of the fiber cladding), and the Y-Half Width is 0.0973. 

Here the Y-Half Width comes from: 0.0625/cos(50°)≈0.0973, and the tilted angle is 50 degree.

![image.png](https://i.loli.net/2021/11/16/KgIp5PeUwXCzlJi.png)
