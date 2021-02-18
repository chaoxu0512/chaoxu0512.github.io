---
layout:     post
title:      Notes-Optimal conditions for SC-based OCT 
subtitle:   
date:       2020-10-22
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Paper and Book
    - Optical Coherence Tomography
---

If you are interested in the original paper `Optimal operational conditions for supercontinuum-based ultrahigh-resolution endoscopic OCT imaging` by Wu Yuan, please refer to Ref. [1].

# 1. General concepts

The laser noise mainly comes from two sources [2]:

- quantum noise, which is related with spontaneous emission in the gain medium.
- technical noise, including excess noise of the pump source, temperature variation, or  the vibrations of the laser resonator.

In optical homodyne detection, the shot noise in the photodetector can be attributed to the discrete nature of photon absorption process [3]. Shot-noise limited means that only the shot noise exists , while other types of noise is absent in the optical signals. For more information, see Ref. [4].

# 2. Some sentences and questions

The line CCD has 2048 pixels and an A-scan rate of up to 70 kHz (i.e., 70k A-scans/s) at a 12 bit resolution. The measured roll-off performance of the spectrometer is ∼ − 13.3 dB/mm.

> how to measure (intensity/ sensitivity) roll off ? 

The fitted blue line with a slope of 1/2 in Fig. 3A shows that with the SuperK source there was a narrow reference arm power region (i.e., between ∼100 and ∼1000 CCD counts) in the middle portion of the noise curve, where the noise followed the square root dependency on the reference arm power level, signifying the shot-noise limited operation region. 

> CCD counts? related with reference arm power level P?
>
> The shot noise is calculated as the square root of the signal, that is $S \propto \sqrt P $. However, why it is linear here?
>
> Why 1000 CCD counts are chosen for the optimal condition? 1. higher optical power leads to higher gain. 2. lower noise floor?

Beyond this region at the upper portion of the noise curve, the laser excess noise dominating region can be identified with a linearly fitted black dash line  of a slope of 1 in the log-log plot.

> why laser excess noise dominates in high power region? Not related with frequency?

The measured detection sensitivity with an incident power of∼9 mW in the sample arm was about −107 dB at a 70 kHz A-scans/s.

> How to calculate the sensitivity here? See Ref.  [5]

An 800 nm endoscopic SD-OCT system that utilized a broadband SC source to enable ultrahigh-resolution, high-sensitivity, and high-speed endoscopic OCT imaging.

> **resolution**: optical design + SC source + reference arm power (shot-noise limited)
>
> **sensitivity**: reference arm power + SC source 
>
> WHAT ANOUT THE INCIDENT POWER OF SAMPLE ARM? 
>
> **speed**: A-scan rate (controlled by ? )
>
> 2 k to 8 k A-scans/frame -> imaging speed up to 35 frames/s, what’s relation with “70 k A-scans/s” ？

# Reference

[1] [Optimal operational conditions for supercontinuum-based ultrahigh-resolution endoscopic OCT imaging](https://www.osapublishing.org/ol/abstract.cfm?uri=ol-41-2-250)

[2] [https://www.rp-photonics.com/laser_noise.html](https://www.rp-photonics.com/laser_noise.html)

[3] [https://en.wikipedia.org/wiki/Shot_noise](https://en.wikipedia.org/wiki/Shot_noise)

[4] [https://www.rp-photonics.com/shot_noise.html](https://www.rp-photonics.com/shot_noise.html)

[5] [Simultaneous dual-band optical coherence tomography in the spectral domain for high resolution *in vivo* imaging](https://doi.org/10.1364/OE.17.019486)

