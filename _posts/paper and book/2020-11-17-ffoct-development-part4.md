---
layout:     post
title:      FFOCT development Part 4
subtitle:   
date:       2020-11-17
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Paper and Book
    - FFOCT
---

## 024 [Full-Field Optical Coherence Microscopy as a tool for intraoperative surgery and tissue selection](https://doi.org/10.1364/NTM.2013.NW5B.1) (2013)

The main difference with standard OCT is that FFOCT records 2D “en face images” (==transverse slices, thickness of about 1 micron==) on megapixel cameras without any transverse scanning. 

3-D images are obtained by moving axially the setup that is compact in order to focus at various depths. 

This configuration allows sharp focusing in the micrometer range (from 0.5 to 1.5 micron depending on the numerical aperture of the microscope).

## 025 [Imaging of non-tumorous and tumorous human brain tissues with full-field optical coherence tomography](https://doi.org/10.1016/j.nicl.2013.04.005) (2013)

For the en face slices, the 3D resolution is about 1um, and the penetration depth is around 200um. A 1 cm^2^ specimen is scanned at a single depth and processed in about 5 min. 

A halogen lamp is used as the light source to illuminate the full field of the sample at a central wavelength of 700nm, with spectral bandwidth of 125nm.

The sample is scanned under a 10 x 0.3 numerical aperture immersion microscope objective.

> Here the immersion medium is a silicone oil of refractive index close to that of water, which is used to optimize the index matching and slow evaporation.

There are some challenges when matching FF-OCT to histology:

- FF-OCT images were captured 20um below the surface, which was comparable to the depth of the histology slices. However **the angle of the inclusion is hard to control**, and thus some difference in the angle of the plane always exists when attempting matching. 
- In addition, the histology slices were 4um in thickness while the thickness of FF-OCT optical slices is 1um. Therefore, **four FF-OCT image slices in 1um were captured and summed to mimic the histology**. However, it would directly degrade the resolution.  

This rapid imaging process is non-invasive and requires neither contrast agent injection nor tissue preparation. The resolution is sufficient to distinguish brain tissue microstructures.

> This study reports for the first time on the feasibility of using FF-OCT in a real-time manner as a label-free non-invasive imaging technique in an intraoperative neurosurgical clinical setting to assess tumorous glial and epileptic margins.

The FF-OCT technique is **not currently suitable for the evaluation of low tumorous infiltration or tumorous margins.** What’s more, it is **difficult to use the FF-OCT technique to estimate the nuclear/cytoplasmic boundaries and the size and form of nuclei**, which prevents precise classification into tumor subtypes and grades. 