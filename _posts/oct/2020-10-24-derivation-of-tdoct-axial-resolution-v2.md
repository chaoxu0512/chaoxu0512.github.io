---
layout:     post
title:      Derivation of TDOCT axial resolution V2
subtitle:   
date:       2020-10-24
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Optical Coherence Tomography
---

The derivation is quite good in Chapter 9 of the book `Biomedical Optics: Principles and Imaging` [1] by Lihong V. Wang,  so I’m not going to repeat again. Here I will add some notes which might be helpful during the derivation. 

------

The formula of coherence length is directly given without specific derivation (Eq. 9.15). 
$$
{l_c} = \frac{{4\ln 2}}{\pi }\frac{{\lambda _0^2}}{{\Delta \lambda }}\label{l_c}
$$
I give an approximate derivation here, and the notation is in accordance with that in the book.
$$
\left\{ \begin{array}{l}
\nu {\rm{ = }}\frac{c}{{{\lambda _0}}}\\
\Delta \nu  = \frac{{c \cdot \Delta \lambda }}{{\lambda _0^2}}\\
{l_c} = c{\tau _c} = \frac{c}{{\Delta \nu }} = \frac{{\lambda _0^2}}{{\Delta \lambda }}
\end{array} \right.
$$
where $\nu $ denotes the frequency of light source, and $\Delta \nu $ denotes the FWHM bandwidth in frequency.

Some coefficients are neglected here. For more specific details, please read the paper `Estimation of longitudinal resolution in optical coherence imaging` [2].

To prove the formula,
$$
{l_c} = 8\ln 2 \cdot \frac{c}{{\Delta \omega }}\label{l_cw}
$$
  we know that  $\omega  = 2\pi \nu $, so it is intuitive to get $\Delta \omega  = 2\pi  \cdot \Delta \nu $. 
$$
\Delta \omega  = 2\pi  \cdot \Delta \nu  = \frac{{2\pi c \cdot \Delta \lambda }}{{\lambda _0^2}}\label{d_w}
$$
 Comparing Eq.$\ref{l_c}$ and Eq. $\ref{d_w}$，and Eq. $\ref{l_cw}$  can be obtained.

------

For Eq. (9.21),  the real number term,
$$
2{\mathop{\rm Re}\nolimits} \left\{ {{E_R}\left( \omega  \right)E_S^*\left( \omega  \right)} \right\} = {\mathop{\rm Re}\nolimits} \left\{ {{E_R}\left( \omega  \right)E_S^*\left( \omega  \right)} \right\} + {\mathop{\rm Re}\nolimits} \left\{ {{E_S}\left( \omega  \right)E_R^*\left( \omega  \right)} \right\}
$$
Pay attention to introduction of the round-trip phase delay $\Delta {\tau _p}$, the round-trip group delay $\Delta {\tau _g}$, phase velocity $v_p$ and group velocity $v_g$,
$$
\left\{ \begin{array}{l}
{v_p} = \frac{{{\omega _0}}}{{k\left( {{\omega _0}} \right)}}\\
\Delta {\tau _p} = \frac{{k\left( {{\omega _0}} \right)}}{{{\omega _0}}}\left( {2\Delta l} \right) = \frac{{2\Delta l}}{{{v_p}}}\\
{v_g} = \frac{1}{{k'\left( {{\omega _0}} \right)}}\\
\Delta {\tau _g} = k'\left( {{\omega _0}} \right)\left( {2\Delta l} \right) = \frac{{2\Delta l}}{{{v_g}}}
\end{array} \right.
$$


Also, think about this expression: If $S\left( \omega  \right)$ is symmetric about ${\omega _0}$, the integral in Eq. (9.36) is real.

> Why is it? You can consider the property of the even function.

After that, Eq. (9.37) can be obtained,
$$
{I_{{\rm{AC}}}} \propto \cos \left( {{\omega _0}\Delta {\tau _p}} \right)\int_{ - \infty }^\infty  {S\left( \omega  \right)\exp \left( { - i\left( {\omega  - {\omega _0}} \right)\Delta {\tau _g}} \right)d\omega } \label{int-g}
$$
Further, if $S\left( \omega  \right)$ is Gaussian, in case that you forget, that is,
$$
S(\omega)=\frac{1}{\sqrt{2 \pi} \sigma_{\omega}} \exp \left(-\frac{\left(\omega-\omega_{0}\right)^{2}}{2 \sigma_{\omega}^{2}}\right)\label{gau}
$$
Substituting Eq. $\ref{gau}$ into Eq. $\ref{int-g}$, 
$$
\begin{array}{l}
{I_{{\rm{AC}}}} \propto \cos \left( {{\omega _0}\Delta {\tau _p}} \right)\int_{ - \infty }^\infty  {\frac{1}{{\sqrt {2\pi } {\sigma _\omega }}}\exp \left( { - \frac{{{{\left( {\omega  - {\omega _0}} \right)}^2}}}{{2\sigma _\omega ^2}}} \right)\exp \left( { - i\left( {\omega  - {\omega _0}} \right)\Delta {\tau _g}} \right)d\omega } \\
 = \frac{{\cos \left( {{\omega _0}\Delta {\tau _p}} \right)}}{{\sqrt {2\pi } {\sigma _\omega }}}\int_{ - \infty }^\infty  {\exp \left[ {\frac{{ - {\omega ^2} - \left( { - 2{\omega _0} + i2\sigma _\omega ^2\Delta {\tau _g}} \right)\omega  - \left( {\omega _0^2 - i2\sigma _\omega ^2\Delta {\tau _g}{\omega _0}} \right)}}{{2\sigma _\omega ^2}}} \right]d\omega } 
\end{array}\label{int-c}
$$
Here, we refer to the general form of [Gaussian integral](https://en.wikipedia.org/wiki/Gaussian_integral) [3]:
$$
\int_{ - \infty }^\infty  {\exp \left( { - a{x^2} - bx - c} \right)dx}  = \sqrt {\frac{\pi }{a}} \exp \left( {\frac{{{b^2}}}{{4a}} - c} \right)\label{gau-i}
$$
Comparing Eq. $\ref{int-c}$ and Eq. $\ref{gau-i}$, we have,
$$
\left\{ \begin{array}{l}
a = \frac{1}{{2\sigma _\omega ^2}}\\
b = \frac{{ - 2{\omega _0} + i2\sigma _\omega ^2\Delta {\tau _g}}}{{2\sigma _\omega ^2}}\\
c = \frac{{\omega _0^2 - i2\sigma _\omega ^2\Delta {\tau _g}{\omega _0}}}{{2\sigma _\omega ^2}}
\end{array} \right.
$$
Next, we do a series of calculation,
$$
\left\{ \begin{array}{l}
{b^2} = \frac{{ - 4\sigma _\omega ^4\Delta \tau _g^2 - i8\sigma _\omega ^2\Delta {\tau _g}{\omega _0} + 4\omega _0^2}}{{4\sigma _\omega ^4}}\\
4a = \frac{2}{{\sigma _\omega ^2}}\\
\frac{{{b^2}}}{{4a}} = \frac{{ - 4\sigma _\omega ^4\Delta \tau _g^2 - i8\sigma _\omega ^2\Delta {\tau _g}{\omega _0} + 4\omega _0^2}}{{8\sigma _\omega ^2}}\\
c = \frac{{4\omega _0^2 - i8\sigma _\omega ^2\Delta {\tau _g}{\omega _0}}}{{8\sigma _\omega ^2}}\\
\frac{{{b^2}}}{{4a}} - c = \frac{{ - \sigma _\omega ^2\Delta \tau _g^2}}{2}\\
\sqrt {\frac{\pi }{a}}  = \sqrt {2\pi } {\sigma _\omega }
\end{array} \right.
$$
Finally, $I_{AC}$ is obtained as below,
$$
{I_{{\rm{AC}}}} \propto \cos \left( {{\omega _0}\Delta {\tau _p}} \right)\exp \left( {\frac{{ - \sigma _\omega ^2\Delta \tau _g^2}}{2}} \right)
$$
It is actually the Eq. (9.38) in the book. 

------

Let’s have a look at Eq (9.41), for the spectrum with a normal distribution, the relationship between its [FWHM](https://en.wikipedia.org/wiki/Full_width_at_half_maximum) and the standard deviation is [4],
$$
\Delta \xi  = 2\sqrt {2\ln 2} {\sigma _\xi }
$$

------

Finally, the axial resolution of OCT in air $\Delta {z_R}$ is obtained,
$$
\Delta {z_R} = \frac{{2\ln 2}}{\pi }\frac{{\lambda _0^2}}{{\Delta \lambda }}
$$
Therefore, the axial resolution in air equals **half** of the coherence length of the source owing to the round-trip propagation of the reference and the sample beams [1].

------

The transverse resolution of OCT in air $\Delta {r_R}$ is also given,
$$
\Delta {r_R} = \frac{{4{\lambda _0}}}{\pi }\frac{f}{D} \approx \frac{{2{\lambda _0}}}{\pi }\frac{1}{{{\rm{NA}}}}
$$
In addition, the depth of focus $\Delta {z_f}$, which is twice of the Rayleigh range,  is given as below,
$$
\Delta {z_f} = \frac{{\pi \Delta r_R^2}}{{2{\lambda _0}}}
$$

# Reference

[1] [Biomedical Optics: Principles and Imaging](https://onlinelibrary.wiley.com/doi/book/10.1002/9780470177013)

[2] [Estimation of longitudinal resolution in optical coherence imaging](https://www.osapublishing.org/abstract.cfm?URI=ao-41-25-5256)

[3] [Gaussian integral](https://en.wikipedia.org/wiki/Gaussian_integral)

[4]  [FWHM](https://en.wikipedia.org/wiki/Full_width_at_half_maximum)

 