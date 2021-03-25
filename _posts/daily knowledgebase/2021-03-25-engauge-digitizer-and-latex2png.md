---
layout:     post
title:      提取图片里的曲线数据&将公式图片插入到Illustrator
subtitle:   
date:       2021-03-25
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Daily Knowledgebase
---
今天分享两个工具，用处见标题。

**1. engauge-digitizer**

项目地址：[https://github.com/markummitchell/engauge-digitizer](https://github.com/markummitchell/engauge-digitizer)

优势：图像化界面，manual很清晰（超级简化版Origin?）。

前几天向Thorlabs要了780HP的色散数据，技术人员给了我一张Matlab绘制的图，没给数据，于是我需要自己从图片里提取数据点。如下图：

<img src="http://imghost.cx0512.com/images/2021/03/25/20210325231212.png" alt="Dispersion of 780HP" style="zoom:67%;" />

软件里的教程很清楚，也简单易用，这里就不多讲了。

<img src="http://imghost.cx0512.com/images/2021/03/25/20210325231643.png" alt="Snipaste_2021-03-25_22-56-05" style="zoom:67%;" />

最后提取的数据点可以保存到csv文件。

**2. latex2png**

项目地址：[http://latex2png.com/](http://latex2png.com/)

优势：简单，会mathtype就行

今天用Illustrator做矢量图，需要在图里加公式字母，我也不想搞一堆代码，编辑ai文件，就StackExchange上找了这个简单好用的工具。具体用法如下：

1)   Draw yourgraphs/images in Illustrator.

2)   Use [http://latex2png.com/](http://latex2png.com/). Type your latexequation in there, then preview at 800 dpi.

3)   Save theimage, then load into Illustrator.

4)   When inIllustrator, select your imported equation image and choose Object --> ImageTrace --> Make and Expand. It is very important to obtain a high dpi imagefor this step to work favorably.

5)   Your equation should now be a vector graphic.

6)   Selectyour new vector graphic equation and choose Object --> Ungroup. This willseparate the white spaces in your equation from the black content that youneed.

7)   Select thewhite spaces and delete them.

8)  You now have a fully editable equation looking exactly like it does in Latex. You canscale/adjust and colour to your requirements.

(来自：[https://bit.ly/3fcY05K](https://bit.ly/3fcY05K))原谅我太懒，也没时间翻译了，但相信都能懂。效果如下：

<img src="http://imghost.cx0512.com/images/2021/03/25/20210325231651.png" alt="Snipaste_2021-03-25_23-04-07" style="zoom:67%;" />



由于是矢量图，再放大，也不会有马赛克的啦。

