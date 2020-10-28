---
layout:     post
title:      Derivation of TDOCT axial resolution V2
subtitle:   
date:       2020-10-24
author:     Chao Xu
header-style: text
hidden: true 
mathjax: true
catalog: true
tags:
    - Optical Coherence Tomography
---

The derivation is quite good in Chapter 9 of the book `Biomedical Optics: Principles and Imaging` [1] by Lihong V. Wang,  so I’m not going to repeat again. Here I will add some notes which might be helpful during the derivation. 

------

The formula of coherence length is directly given without specific derivation (Eq. 9.15). 

![{l_c} = \frac{{4\ln 2}}{\pi }\frac{{\lambda _0^2}}{{\Delta \lambda }} \leftrightarrow (1)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%7Bl_c%7D%20%3D%20%5Cfrac%7B%7B4%5Cln%202%7D%7D%7B%5Cpi%20%7D%5Cfrac%7B%7B%5Clambda%20_0%5E2%7D%7D%7B%7B%5CDelta%20%5Clambda%20%7D%7D%20%5Cleftrightarrow%20%281%29)

I give an approximate derivation here, and the notation is in accordance with that in the book.

$$\left\{ {\begin{array}{*{20}{l}}{\nu {\rm{ = }}\frac{c}{{{\lambda _0}}}}\\{\Delta \nu  = \frac{{c \cdot \Delta \lambda }}{{\lambda _0^2}}}\\{{l_c} = c{\tau _c} = \frac{c}{{\Delta \nu }} = \frac{{\lambda _0^2}}{{\Delta \lambda }}}\end{array}} \right. \leftrightarrow (2)$$

![\left\{ {\begin{array}{lllllllllllllll} {\nu {\rm{ = }}\frac{c}{{{\lambda _0}}}}\\ {\Delta \nu  = \frac{{c \cdot \Delta \lambda }}{{\lambda _0^2}}}\\ {{l_c} = c{\tau _c} = \frac{c}{{\Delta \nu }} = \frac{{\lambda _0^2}}{{\Delta \lambda }}} \end{array}} \right. \leftrightarrow (2)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%5Cleft%5C%7B%20%7B%5Cbegin%7Barray%7D%7Blllllllllllllll%7D%0A%7B%5Cnu%20%7B%5Crm%7B%20%3D%20%7D%7D%5Cfrac%7Bc%7D%7B%7B%7B%5Clambda%20_0%7D%7D%7D%7D%5C%5C%0A%7B%5CDelta%20%5Cnu%20%20%3D%20%5Cfrac%7B%7Bc%20%5Ccdot%20%5CDelta%20%5Clambda%20%7D%7D%7B%7B%5Clambda%20_0%5E2%7D%7D%7D%5C%5C%0A%7B%7Bl_c%7D%20%3D%20c%7B%5Ctau%20_c%7D%20%3D%20%5Cfrac%7Bc%7D%7B%7B%5CDelta%20%5Cnu%20%7D%7D%20%3D%20%5Cfrac%7B%7B%5Clambda%20_0%5E2%7D%7D%7B%7B%5CDelta%20%5Clambda%20%7D%7D%7D%0A%5Cend%7Barray%7D%7D%20%5Cright.%20%5Cleftrightarrow%20%282%29)

where $\nu $ denotes the frequency of light source, and $\Delta \nu $ denotes the FWHM bandwidth in frequency.

Some coefficients are neglected here. For more specific details, please read the paper `Estimation of longitudinal resolution in optical coherence imaging` [2].

To prove the formula,

![{l_c} = 8\ln 2 \cdot \frac{c}{{\Delta \omega }} \leftrightarrow (3)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%7Bl_c%7D%20%3D%208%5Cln%202%20%5Ccdot%20%5Cfrac%7Bc%7D%7B%7B%5CDelta%20%5Comega%20%7D%7D%20%5Cleftrightarrow%20%283%29)

  we know that  $\omega  = 2\pi \nu $, so it is intuitive to get $\Delta \omega  = 2\pi  \cdot \Delta \nu $. 

![\Delta \omega  = 2\pi  \cdot \Delta \nu  = \frac{{2\pi c \cdot \Delta \lambda }}{{\lambda _0^2}} \leftrightarrow (4)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%5CDelta%20%5Comega%20%20%3D%202%5Cpi%20%20%5Ccdot%20%5CDelta%20%5Cnu%20%20%3D%20%5Cfrac%7B%7B2%5Cpi%20c%20%5Ccdot%20%5CDelta%20%5Clambda%20%7D%7D%7B%7B%5Clambda%20_0%5E2%7D%7D%20%5Cleftrightarrow%20%284%29)

 Comparing Eq. 1 and Eq. 4，and Eq. 3  can be obtained.

------

For Eq. (9.21),  the real number term,

![2{\rm{Re}}\left\{ {{E_R}\left( \omega  \right)E_S^*\left( \omega  \right)} \right\} = {\rm{Re}}\left\{ {{E_R}\left( \omega  \right)E_S^*\left( \omega  \right)} \right\} + {\rm{Re}}\left\{ {{E_S}\left( \omega  \right)E_R^*\left( \omega  \right)} \right\} \leftrightarrow (5)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=2%7B%5Crm%7BRe%7D%7D%5Cleft%5C%7B%20%7B%7BE_R%7D%5Cleft%28%20%5Comega%20%20%5Cright%29E_S%5E%2A%5Cleft%28%20%5Comega%20%20%5Cright%29%7D%20%5Cright%5C%7D%20%3D%20%7B%5Crm%7BRe%7D%7D%5Cleft%5C%7B%20%7B%7BE_R%7D%5Cleft%28%20%5Comega%20%20%5Cright%29E_S%5E%2A%5Cleft%28%20%5Comega%20%20%5Cright%29%7D%20%5Cright%5C%7D%20%2B%20%7B%5Crm%7BRe%7D%7D%5Cleft%5C%7B%20%7B%7BE_S%7D%5Cleft%28%20%5Comega%20%20%5Cright%29E_R%5E%2A%5Cleft%28%20%5Comega%20%20%5Cright%29%7D%20%5Cright%5C%7D%20%5Cleftrightarrow%20%285%29)

Pay attention to introduction of the round-trip phase delay $\Delta {\tau _p}$, the round-trip group delay $\Delta {\tau _g}$, phase velocity $v_p$ and group velocity $v_g$,

![\left\{ {\begin{array}{lllllllllllllll} {{v_p} = \frac{{{\omega _0}}}{{k\left( {{\omega _0}} \right)}}}\\ {\Delta {\tau _p} = \frac{{k\left( {{\omega _0}} \right)}}{{{\omega _0}}}\left( {2\Delta l} \right) = \frac{{2\Delta l}}{{{v_p}}}}\\ {{v_g} = \frac{1}{{k'\left( {{\omega _0}} \right)}}}\\ {\Delta {\tau _g} = k'\left( {{\omega _0}} \right)\left( {2\Delta l} \right) = \frac{{2\Delta l}}{{{v_g}}}} \end{array}} \right. \leftrightarrow (6)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%5Cleft%5C%7B%20%7B%5Cbegin%7Barray%7D%7Blllllllllllllll%7D%0A%7B%7Bv_p%7D%20%3D%20%5Cfrac%7B%7B%7B%5Comega%20_0%7D%7D%7D%7B%7Bk%5Cleft%28%20%7B%7B%5Comega%20_0%7D%7D%20%5Cright%29%7D%7D%7D%5C%5C%0A%7B%5CDelta%20%7B%5Ctau%20_p%7D%20%3D%20%5Cfrac%7B%7Bk%5Cleft%28%20%7B%7B%5Comega%20_0%7D%7D%20%5Cright%29%7D%7D%7B%7B%7B%5Comega%20_0%7D%7D%7D%5Cleft%28%20%7B2%5CDelta%20l%7D%20%5Cright%29%20%3D%20%5Cfrac%7B%7B2%5CDelta%20l%7D%7D%7B%7B%7Bv_p%7D%7D%7D%7D%5C%5C%0A%7B%7Bv_g%7D%20%3D%20%5Cfrac%7B1%7D%7B%7Bk%27%5Cleft%28%20%7B%7B%5Comega%20_0%7D%7D%20%5Cright%29%7D%7D%7D%5C%5C%0A%7B%5CDelta%20%7B%5Ctau%20_g%7D%20%3D%20k%27%5Cleft%28%20%7B%7B%5Comega%20_0%7D%7D%20%5Cright%29%5Cleft%28%20%7B2%5CDelta%20l%7D%20%5Cright%29%20%3D%20%5Cfrac%7B%7B2%5CDelta%20l%7D%7D%7B%7B%7Bv_g%7D%7D%7D%7D%0A%5Cend%7Barray%7D%7D%20%5Cright.%20%5Cleftrightarrow%20%286%29)


Also, think about this expression: If $S\left( \omega  \right)$ is symmetric about ${\omega _0}$, the integral in Eq. (9.36) is real.

> Why is it? You can consider the property of the even function.

After that, Eq. (9.37) can be obtained,

![{I_{{\rm{AC}}}} \propto \cos \left( {{\omega _0}\Delta {\tau _p}} \right)\int_{ - \infty }^\infty  {S\left( \omega  \right)\exp \left( { - i\left( {\omega  - {\omega _0}} \right)\Delta {\tau _g}} \right)d\omega }  \leftrightarrow (7)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%7BI_%7B%7B%5Crm%7BAC%7D%7D%7D%7D%20%5Cpropto%20%5Ccos%20%5Cleft%28%20%7B%7B%5Comega%20_0%7D%5CDelta%20%7B%5Ctau%20_p%7D%7D%20%5Cright%29%5Cint_%7B%20-%20%5Cinfty%20%7D%5E%5Cinfty%20%20%7BS%5Cleft%28%20%5Comega%20%20%5Cright%29%5Cexp%20%5Cleft%28%20%7B%20-%20i%5Cleft%28%20%7B%5Comega%20%20-%20%7B%5Comega%20_0%7D%7D%20%5Cright%29%5CDelta%20%7B%5Ctau%20_g%7D%7D%20%5Cright%29d%5Comega%20%7D%20%20%5Cleftrightarrow%20%287%29)

Further, if $S\left( \omega  \right)$ is Gaussian, in case that you forget, that is,

![S(\omega ) = \frac{1}{{\sqrt {2\pi } {\sigma _\omega }}}\exp \left( { - \frac{{{{\left( {\omega  - {\omega _0}} \right)}^2}}}{{2\sigma _\omega ^2}}} \right) \leftrightarrow (8)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=S%28%5Comega%20%29%20%3D%20%5Cfrac%7B1%7D%7B%7B%5Csqrt%20%7B2%5Cpi%20%7D%20%7B%5Csigma%20_%5Comega%20%7D%7D%7D%5Cexp%20%5Cleft%28%20%7B%20-%20%5Cfrac%7B%7B%7B%7B%5Cleft%28%20%7B%5Comega%20%20-%20%7B%5Comega%20_0%7D%7D%20%5Cright%29%7D%5E2%7D%7D%7D%7B%7B2%5Csigma%20_%5Comega%20%5E2%7D%7D%7D%20%5Cright%29%20%5Cleftrightarrow%20%288%29)

Substituting Eq. 8 into Eq. 7, 

![\begin{array}{lllllllllllllll} {{I_{{\rm{AC}}}} \propto \cos \left( {{\omega _0}\Delta {\tau _p}} \right)\int_{ - \infty }^\infty  {\frac{1}{{\sqrt {2\pi } {\sigma _\omega }}}\exp \left( { - \frac{{{{\left( {\omega  - {\omega _0}} \right)}^2}}}{{2\sigma _\omega ^2}}} \right)\exp \left( { - i\left( {\omega  - {\omega _0}} \right)\Delta {\tau _g}} \right)d\omega } }\\ { = \frac{{\cos \left( {{\omega _0}\Delta {\tau _p}} \right)}}{{\sqrt {2\pi } {\sigma _\omega }}}\int_{ - \infty }^\infty  {\exp \left[ {\frac{{ - {\omega ^2} - \left( { - 2{\omega _0} + i2\sigma _\omega ^2\Delta {\tau _g}} \right)\omega  - \left( {\omega _0^2 - i2\sigma _\omega ^2\Delta {\tau _g}{\omega _0}} \right)}}{{2\sigma _\omega ^2}}} \right]d\omega } } \end{array} \leftrightarrow (9)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%5Cbegin%7Barray%7D%7Blllllllllllllll%7D%0A%7B%7BI_%7B%7B%5Crm%7BAC%7D%7D%7D%7D%20%5Cpropto%20%5Ccos%20%5Cleft%28%20%7B%7B%5Comega%20_0%7D%5CDelta%20%7B%5Ctau%20_p%7D%7D%20%5Cright%29%5Cint_%7B%20-%20%5Cinfty%20%7D%5E%5Cinfty%20%20%7B%5Cfrac%7B1%7D%7B%7B%5Csqrt%20%7B2%5Cpi%20%7D%20%7B%5Csigma%20_%5Comega%20%7D%7D%7D%5Cexp%20%5Cleft%28%20%7B%20-%20%5Cfrac%7B%7B%7B%7B%5Cleft%28%20%7B%5Comega%20%20-%20%7B%5Comega%20_0%7D%7D%20%5Cright%29%7D%5E2%7D%7D%7D%7B%7B2%5Csigma%20_%5Comega%20%5E2%7D%7D%7D%20%5Cright%29%5Cexp%20%5Cleft%28%20%7B%20-%20i%5Cleft%28%20%7B%5Comega%20%20-%20%7B%5Comega%20_0%7D%7D%20%5Cright%29%5CDelta%20%7B%5Ctau%20_g%7D%7D%20%5Cright%29d%5Comega%20%7D%20%7D%5C%5C%0A%7B%20%3D%20%5Cfrac%7B%7B%5Ccos%20%5Cleft%28%20%7B%7B%5Comega%20_0%7D%5CDelta%20%7B%5Ctau%20_p%7D%7D%20%5Cright%29%7D%7D%7B%7B%5Csqrt%20%7B2%5Cpi%20%7D%20%7B%5Csigma%20_%5Comega%20%7D%7D%7D%5Cint_%7B%20-%20%5Cinfty%20%7D%5E%5Cinfty%20%20%7B%5Cexp%20%5Cleft%5B%20%7B%5Cfrac%7B%7B%20-%20%7B%5Comega%20%5E2%7D%20-%20%5Cleft%28%20%7B%20-%202%7B%5Comega%20_0%7D%20%2B%20i2%5Csigma%20_%5Comega%20%5E2%5CDelta%20%7B%5Ctau%20_g%7D%7D%20%5Cright%29%5Comega%20%20-%20%5Cleft%28%20%7B%5Comega%20_0%5E2%20-%20i2%5Csigma%20_%5Comega%20%5E2%5CDelta%20%7B%5Ctau%20_g%7D%7B%5Comega%20_0%7D%7D%20%5Cright%29%7D%7D%7B%7B2%5Csigma%20_%5Comega%20%5E2%7D%7D%7D%20%5Cright%5Dd%5Comega%20%7D%20%7D%0A%5Cend%7Barray%7D%20%5Cleftrightarrow%20%289%29)

Here, we refer to the general form of [Gaussian integral](https://en.wikipedia.org/wiki/Gaussian_integral) [3]:

![\int_{ - \infty }^\infty  {\exp \left( { - a{x^2} - bx - c} \right)dx}  = \sqrt {\frac{\pi }{a}} \exp \left( {\frac{{{b^2}}}{{4a}} - c} \right) \leftrightarrow (10)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%5Cint_%7B%20-%20%5Cinfty%20%7D%5E%5Cinfty%20%20%7B%5Cexp%20%5Cleft%28%20%7B%20-%20a%7Bx%5E2%7D%20-%20bx%20-%20c%7D%20%5Cright%29dx%7D%20%20%3D%20%5Csqrt%20%7B%5Cfrac%7B%5Cpi%20%7D%7Ba%7D%7D%20%5Cexp%20%5Cleft%28%20%7B%5Cfrac%7B%7B%7Bb%5E2%7D%7D%7D%7B%7B4a%7D%7D%20-%20c%7D%20%5Cright%29%20%5Cleftrightarrow%20%2810%29)

Comparing Eq. 9 and Eq. 10, we have,

![\left\{ {\begin{array}{lllllllllllllll} {a = \frac{1}{{2\sigma _\omega ^2}}}\\ {b = \frac{{ - 2{\omega _0} + i2\sigma _\omega ^2\Delta {\tau _g}}}{{2\sigma _\omega ^2}}}\\ {c = \frac{{\omega _0^2 - i2\sigma _\omega ^2\Delta {\tau _g}{\omega _0}}}{{2\sigma _\omega ^2}}} \end{array}} \right. \leftrightarrow (11)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%5Cleft%5C%7B%20%7B%5Cbegin%7Barray%7D%7Blllllllllllllll%7D%0A%7Ba%20%3D%20%5Cfrac%7B1%7D%7B%7B2%5Csigma%20_%5Comega%20%5E2%7D%7D%7D%5C%5C%0A%7Bb%20%3D%20%5Cfrac%7B%7B%20-%202%7B%5Comega%20_0%7D%20%2B%20i2%5Csigma%20_%5Comega%20%5E2%5CDelta%20%7B%5Ctau%20_g%7D%7D%7D%7B%7B2%5Csigma%20_%5Comega%20%5E2%7D%7D%7D%5C%5C%0A%7Bc%20%3D%20%5Cfrac%7B%7B%5Comega%20_0%5E2%20-%20i2%5Csigma%20_%5Comega%20%5E2%5CDelta%20%7B%5Ctau%20_g%7D%7B%5Comega%20_0%7D%7D%7D%7B%7B2%5Csigma%20_%5Comega%20%5E2%7D%7D%7D%0A%5Cend%7Barray%7D%7D%20%5Cright.%20%5Cleftrightarrow%20%2811%29)

Next, we do a series of calculation,

![\left\{ {\begin{array}{lllllllllllllll} {{b^2} = \frac{{ - 4\sigma _\omega ^4\Delta \tau _g^2 - i8\sigma _\omega ^2\Delta {\tau _g}{\omega _0} + 4\omega _0^2}}{{4\sigma _\omega ^4}}}\\ {4a = \frac{2}{{\sigma _\omega ^2}}}\\ {\frac{{{b^2}}}{{4a}} = \frac{{ - 4\sigma _\omega ^4\Delta \tau _g^2 - i8\sigma _\omega ^2\Delta {\tau _g}{\omega _0} + 4\omega _0^2}}{{8\sigma _\omega ^2}}}\\ {c = \frac{{4\omega _0^2 - i8\sigma _\omega ^2\Delta {\tau _g}{\omega _0}}}{{8\sigma _\omega ^2}}}\\ {\frac{{{b^2}}}{{4a}} - c = \frac{{ - \sigma _\omega ^2\Delta \tau _g^2}}{2}}\\ {\sqrt {\frac{\pi }{a}}  = \sqrt {2\pi } {\sigma _\omega }} \end{array}} \right. \leftrightarrow (12)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%5Cleft%5C%7B%20%7B%5Cbegin%7Barray%7D%7Blllllllllllllll%7D%0A%7B%7Bb%5E2%7D%20%3D%20%5Cfrac%7B%7B%20-%204%5Csigma%20_%5Comega%20%5E4%5CDelta%20%5Ctau%20_g%5E2%20-%20i8%5Csigma%20_%5Comega%20%5E2%5CDelta%20%7B%5Ctau%20_g%7D%7B%5Comega%20_0%7D%20%2B%204%5Comega%20_0%5E2%7D%7D%7B%7B4%5Csigma%20_%5Comega%20%5E4%7D%7D%7D%5C%5C%0A%7B4a%20%3D%20%5Cfrac%7B2%7D%7B%7B%5Csigma%20_%5Comega%20%5E2%7D%7D%7D%5C%5C%0A%7B%5Cfrac%7B%7B%7Bb%5E2%7D%7D%7D%7B%7B4a%7D%7D%20%3D%20%5Cfrac%7B%7B%20-%204%5Csigma%20_%5Comega%20%5E4%5CDelta%20%5Ctau%20_g%5E2%20-%20i8%5Csigma%20_%5Comega%20%5E2%5CDelta%20%7B%5Ctau%20_g%7D%7B%5Comega%20_0%7D%20%2B%204%5Comega%20_0%5E2%7D%7D%7B%7B8%5Csigma%20_%5Comega%20%5E2%7D%7D%7D%5C%5C%0A%7Bc%20%3D%20%5Cfrac%7B%7B4%5Comega%20_0%5E2%20-%20i8%5Csigma%20_%5Comega%20%5E2%5CDelta%20%7B%5Ctau%20_g%7D%7B%5Comega%20_0%7D%7D%7D%7B%7B8%5Csigma%20_%5Comega%20%5E2%7D%7D%7D%5C%5C%0A%7B%5Cfrac%7B%7B%7Bb%5E2%7D%7D%7D%7B%7B4a%7D%7D%20-%20c%20%3D%20%5Cfrac%7B%7B%20-%20%5Csigma%20_%5Comega%20%5E2%5CDelta%20%5Ctau%20_g%5E2%7D%7D%7B2%7D%7D%5C%5C%0A%7B%5Csqrt%20%7B%5Cfrac%7B%5Cpi%20%7D%7Ba%7D%7D%20%20%3D%20%5Csqrt%20%7B2%5Cpi%20%7D%20%7B%5Csigma%20_%5Comega%20%7D%7D%0A%5Cend%7Barray%7D%7D%20%5Cright.%20%5Cleftrightarrow%20%2812%29)

Finally, $I_{AC}$ is obtained as below,

![{I_{{\rm{AC}}}} \propto \cos \left( {{\omega _0}\Delta {\tau _p}} \right)\exp \left( {\frac{{ - \sigma _\omega ^2\Delta \tau _g^2}}{2}} \right) \leftrightarrow (13)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%7BI_%7B%7B%5Crm%7BAC%7D%7D%7D%7D%20%5Cpropto%20%5Ccos%20%5Cleft%28%20%7B%7B%5Comega%20_0%7D%5CDelta%20%7B%5Ctau%20_p%7D%7D%20%5Cright%29%5Cexp%20%5Cleft%28%20%7B%5Cfrac%7B%7B%20-%20%5Csigma%20_%5Comega%20%5E2%5CDelta%20%5Ctau%20_g%5E2%7D%7D%7B2%7D%7D%20%5Cright%29%20%5Cleftrightarrow%20%2813%29)

It is actually the Eq. (9.38) in the book. 

------

Let’s have a look at Eq (9.41), for the spectrum with a normal distribution, the relationship between its [FWHM](https://en.wikipedia.org/wiki/Full_width_at_half_maximum) and the standard deviation is [4],

![\Delta \xi  = 2\sqrt {2\ln 2} {\sigma _\xi } \leftrightarrow (14)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%5CDelta%20%5Cxi%20%20%3D%202%5Csqrt%20%7B2%5Cln%202%7D%20%7B%5Csigma%20_%5Cxi%20%7D%20%5Cleftrightarrow%20%2814%29)

------

Finally, the axial resolution of OCT in air $\Delta {z_R}$ is obtained,

![\Delta {z_R} = \frac{{2\ln 2}}{\pi }\frac{{\lambda _0^2}}{{\Delta \lambda }} \leftrightarrow (15)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%5CDelta%20%7Bz_R%7D%20%3D%20%5Cfrac%7B%7B2%5Cln%202%7D%7D%7B%5Cpi%20%7D%5Cfrac%7B%7B%5Clambda%20_0%5E2%7D%7D%7B%7B%5CDelta%20%5Clambda%20%7D%7D%20%5Cleftrightarrow%20%2815%29)

Therefore, the axial resolution in air equals **half** of the coherence length of the source owing to the round-trip propagation of the reference and the sample beams [1].

------

The transverse resolution of OCT in air $\Delta {r_R}$ is also given,

![\Delta {r_R} = \frac{{4{\lambda _0}}}{\pi }\frac{f}{D} \approx \frac{{2{\lambda _0}}}{\pi }\frac{1}{{{\rm{NA}}}} \leftrightarrow (16)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%5CDelta%20%7Br_R%7D%20%3D%20%5Cfrac%7B%7B4%7B%5Clambda%20_0%7D%7D%7D%7B%5Cpi%20%7D%5Cfrac%7Bf%7D%7BD%7D%20%5Capprox%20%5Cfrac%7B%7B2%7B%5Clambda%20_0%7D%7D%7D%7B%5Cpi%20%7D%5Cfrac%7B1%7D%7B%7B%7B%5Crm%7BNA%7D%7D%7D%7D%20%5Cleftrightarrow%20%2816%29)

In addition, the depth of focus $\Delta {z_f}$, which is twice of the Rayleigh range,  is given as below,

![\Delta {z_f} = \frac{{\pi \Delta r_R^2}}{{2{\lambda _0}}} \leftrightarrow (17)](http://chart.apis.google.com/chart?cht=tx&chs=1x0&chf=bg,s,FFFFFF00&chco=000000&chl=%5CDelta%20%7Bz_f%7D%20%3D%20%5Cfrac%7B%7B%5Cpi%20%5CDelta%20r_R%5E2%7D%7D%7B%7B2%7B%5Clambda%20_0%7D%7D%7D%20%5Cleftrightarrow%20%2817%29)

# Reference

[1] [Biomedical Optics: Principles and Imaging](https://onlinelibrary.wiley.com/doi/book/10.1002/9780470177013)

[2] [Estimation of longitudinal resolution in optical coherence imaging](https://www.osapublishing.org/abstract.cfm?URI=ao-41-25-5256)

[3] [Gaussian integral](https://en.wikipedia.org/wiki/Gaussian_integral)

[4]  [FWHM](https://en.wikipedia.org/wiki/Full_width_at_half_maximum)

 