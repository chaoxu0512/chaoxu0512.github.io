---
layout:     post
title:      VS2008中"breakpoint will not currently be hit. No symbols have been loaded for this document"的解决方法
subtitle:   
date:       2021-05-04
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - daily knowledgebase
---

我的解决方案：

1. Right-click project
2. Select the Properties
3. Select C/C++ ->General
4. Set Debug Information Format to `program Database(/Zi)`
5. Check Linker->Debugging->Generate Debug info: `Yes`.

参考：[https://stackoverflow.com/questions/5181401/vs-2008-breakpoint-will-not-currently-be-hit-no-symbols-have-been-loaded-for-th](https://stackoverflow.com/questions/5181401/vs-2008-breakpoint-will-not-currently-be-hit-no-symbols-have-been-loaded-for-th)
