---
layout:     post
title:      FFOCT development Part 6
subtitle:   
date:       2020-12-14
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Optical Coherence Tomography
---

#### 030 [Fingerprint imaging from the inside of a finger with full-field optical coherence tomography](https://doi.org/10.1364/boe.6.004465) (2015)

An oblique FF-OCT method (o-FF-OCT) is proposed for real-time live fingerprint imaging applications. This o-FF-OCT enables imaging all the layers in one image from which the distances to the surface of each layer can be predetermined. Basically, it is achieved by tilting the reflector in the reference arm, and thus shifts the reference beam position. Knowing the tilt and the image depth at which the oblique image was acquired, it can be calculated where the most intense signal was located in the internal fingerprint layer.

This technique might be a convenient way to quickly determine the depth of each skin layer of interest since it vary from person to person and from finger to finger. 

It is important to be able to scan fingerprints fast enough so that finger movement during the acquisition would not compromise the quality of fingerprint image. In the experiment, the images can be obtained within a second (averaged on ten en face images), which is adequate for live fingerprint  imaging applications. With faster InGaAs camera, the  acquisition time can be further reduced.

#### 031 [Transmission glass-like aberrations correction for full-field OCT Imaging](https://doi.org/10.1364/AOMS.2015.AOTh3D.4) (2015)

In this article, a compact transmissive liquid crystal spatial light modulator (LCSLM) is coupled to a full-field OCT imaging system.  It is verified that the LCSLM can be used to induce and correct aberrations. The metric is based on the FFOCT image quality.

#### 032 [Dark-field full-field optical coherence tomography](https://doi.org/10.1364/OL.40.003272) (2015)

Dark-field full-field OCT (d-FFO-OCT) was realized by putting a block in the central part of the pupil-conjugated plane and replacing the reference mirror with a blazed reflective diffraction grating.

d-FF-OCT enabled recording high contrast OCT images at a coverslip-tissue interface by suppressing specular reflections by at least two orders of magnitude, which otherwise severely reduce image contrast.

<p align="center">
<img src="https://i.loli.net/2020/12/15/qTiYlfEn8WZ7gv2.png" width=300pix>
</p>
<p style="text-align:center;">Fig.1. Schematic diagram of d-FF-OCT. Scattered light from a specimen (gray) interferes on a camera with the reference beam (light green). Specular reflections from a specimen (and the zeroth-order from the blazed grating) are obstructed by a block in the pupil- conjugate plane (pupil’). The reference beam is dispersed spectrally on the pupil-conjugated plane, as shown in the lower inset. The aper- ture diaphragm is matched to the size ofthe block of2 mm. Note that in the diagram, for the sake of simplicity, the beam path is shown for the spatially and temporally coherent illumination case—only one ray, originating at the center of the LED, is drawn, which also does not experience dispersion in the pupil’ plane. Thus, the beam is depicted to focus to a spot on a pupil plane, rather than to a 2 mm disk, as is shown in the lower inset. Upper inset: coherence gate tilt with a mirror and a grating.(From the original paper)</p>

d-FF-OCT enables acquisition of optically sectioned dark-field images, which helps to get rid of the unwanted reflected and scattered light by either physically blocking it or gating it through interferometric detection.

#### 033 [Assessment of Sentinel Node Biopsies With Full-Field Optical Coherence Tomography](https://doi.org/10.1177/1533034615575817) (2016)

The short coherence length leads to an axial resolution of 1um. The immersion objectives with the numerical aperture of 0.3 leads to a lateral resolution of 1.6um. The penetration depth in the lymph nodes is of the order of 200-300um. A 1cm x 1cm stitched field is captured within 10 minutes, and a 3D stack of 200um x 1mm x 1mm is also captured less than 5 minutes.

The FFOCT is a comparable technique to the Frozen Section analysis. FFOCT holds the advantage of simplicity, since no expertise is necessary for the image acquisition.   For the standard FS preparation, technical expertise is required to obtain good-quality slides. In addition, FFOCT does not consume tissue. It showed very good sensitivity and specificity values (between 83% and 94%) on the blind benign/malignant diagnosis by a pathologist and a nonpathologist. It is expected that analysis of ex vivo sentinel node biopsies with FFOCT may have potential to replace FS analysis

#### 034 [Full-field spatially incoherent illumination interferometry: a spatial resolution almost insensitive to aberrations](https://doi.org/10.1364/ol.41.003920) (2016)

It was found that: with spatially incoherent illumination, the resolution of FFOCT  is almost insensitive to aberrations. The aberrations mostly induce a reduction of the signal that leads to a loss of the signal-to-noise ratio without broadening the system point spread function.

#### 035 [Adaptive optics full-field optical coherence tomography](https://doi.org/10.1117/1.jbo.21.12.121505) (2016)

In this paper, a transmissive liquid crystal spatial light modulator (LCSLM) was coupled to a FFOCT setup to induce or correct aberrations. 

Some key points are listed:

- Since low-order aberrations are dominant in the imaging system, pupil conjugation was discarded,  instead nonconjugated configuration was adopted.
- The point spread function of the imaging system is almost insensitive to the aberrations, and mostly they tend to reduce the signal level.  
- An image based optimization algorithm was applied to recover the aberrated images by the metric of FFOCT image intensity.

To verify the whole process of adaptive optics aberration corrections, two experiments were demonstrated of an USAF resolution target and biological samples for LCSLM-induced and sample-induced wavefront distortions.  

For the LCSLM-induced aberrations, the corrected signal level reaches the mean intensity to 78.0% ± 2.2% of the nonaberrated FFOCT image, corresponding to a Strehl of 0.61 ± 0.035. The result is slightly inferior but acceptable compared with conjugated AO experiment, which results in a corrected FFOCT image signal level reaching 84.3% ± 2.1% of the nonaberrated image.

For the sample-induced aberrations, the whole correction process results in 13.3% improvement of the metric function.

Considering the potential of this AO-FFOCT system for retinal imaging, aberrations correction might be restricted to main aberrations (e.g., focus and astigmatism) that will improve the SNR and skip the high-order aberrations.