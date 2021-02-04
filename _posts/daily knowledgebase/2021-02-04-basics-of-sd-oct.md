---
layout:     post
title:      SDOCT中的两臂和spectrometer
subtitle:   Optical Coherence Tomography - Technology and Applications
date:       2021-02-04
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Daily Knowledgebase
---

**1.**在Optical Coherence Tomography - Technology and Applications的第36页中，提到：

*The interference of the two beams will have a spectral modulation as a function of frequency which can be measured using a spectrometer. The periodicity of this modulation will be inversely related to the echo time delay. Therefore, different echo delays will produce different frequency modulations. The echo delays can be measured by rescaling the spectrometer output from wavelength to frequency and then Fourier transforming the interference signal.*

也就是说，更长的optical path delay，就对应着频域上的更高频分量。

2.在Optical Coherence Tomography - Technology and Applications的第37页中，提到：

*The spectrometer is typically a refractive spectrometer, using lenses for collimating the optical fiber output onto a diffraction grating and for focusing the angularly dispersed spectrum on the line scan camera. Transmission diffraction gratings are typically used because the diffraction efficiencies are less polarization dependent than reflective gratings. The spectrometer generates an interference spectrum which is a function of wavelength; therefore, the spectrum must be numerically resampled from wavelength to frequency or wavenumber k before Fourier transforming. The Fourier transform of the spectrum generates the axial scan.*

这一段基本讲了spectrometer的作用。