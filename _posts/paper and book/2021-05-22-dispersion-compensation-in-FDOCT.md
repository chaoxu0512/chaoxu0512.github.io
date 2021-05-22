---
layout:     post
title:      Dispersion compensation in OCT
subtitle:   
date:       2021-05-22
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Paper and Book
    - Optical Coherence Tomography
    - Fujimoto Paper
---

1 [Ultrahigh-resolution, high-speed, Fourier domain optical coherence tomography and methods for dispersion compensation](https://doi.org/10.1364/OPEX.12.002404)

In OCT, dispersion compensation is usually performed by matching the optical materials and path lengths in the two interferometer arms. Dispersion can also be compensated by using numerical techniques. 

---

Principle of SD-OCT: 

The sample is illuminated with broadband light. Backreflected or backscattered light signals from different depths that correspond to different delays are brought to interference with light from a reference path with a known delay. The interference produces fringes, which are detected by a spectrometer using a high-speed multi-element CCD or photodiode array detector. The delay and magnitude of the optical reflections from the sample can be detected by Fourier transforming the spectral interference signal.

---

Frequency and delay-dependent phase:  
$$
S_{\text {int }}(\omega)=2 \operatorname{Re}\left\{E_{R}(\omega)^{*} E_{S}(\omega)\right\}=2 \operatorname{Re}\left\{\sum_{n} \sqrt{I_{n}(\omega) I_{r}(\omega)} \exp \left[i\left(\omega \tau_{n}+\Phi\left(\omega, \tau_{n}\right)\right)\right]\right\}
$$
$I_n$ is the intensity of light reflected from the n-th layer in the sample, $I_r$ is the intensity of light reflected from the reference arm, and $τ_n$ is the optical group delay of the n-th reflection, relative to the reference light path. <u>Φ(ω,$τ_n$) is a general frequency and delay-dependent phase that includes higher order dispersive terms.</u>  

Theoretical axial resolution:
$$
\Delta z=\frac{2 \ln 2}{\pi} \frac{\lambda_{0}^{2}}{\Delta \lambda}
$$
where ∆λ is the full width half maximum (FWHM) of the light source and $λ_0$ is the center wavelength.  

---

