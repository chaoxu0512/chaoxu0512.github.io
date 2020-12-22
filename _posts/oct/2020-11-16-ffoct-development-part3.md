---
layout:     post
title:      FFOCT development Part 3
subtitle:   
date:       2020-11-16
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Optical Coherence Tomography
---

#### 020 [Flexible and rigid endoscopy for high-resolution in-depth imaging with Full-Field OCT](https://www.osapublishing.org/abstract.cfm?URI=BIOMED-2012-BTu4B.4) (2012)

The system, working in a common path,  uses two coupled interferometers, a processing interferometer external to the probe and a distal interferometer at the end of the probe in contact with the sample. 

> The probe is not part of an interferometer arm, and is only used to transport an image. Therefore, it is insensitive to the environment. The system is suitable for in situ and in vivo imaging.

> Common path: the interference occurs between the light backscattered from various depths within the tissue and the reference light reflected at the tip of the probe.

A Xenon arc lamp as the light source, with very low temporal (ensure a good axial resolution) and spatial (decrease cross-talk effects) resolution. 

> The source spectrum is not as smooth as that of a thermal light source(a tungsten filament), but is with much higher luminance and power level.

> Crosstalk: the signal can pass from one core to an adjacent one, thus creating a distribution of path length differences within the bundle, which induces a parasitic interferometric signal superimposed to the real interferometric signal coming from the sample.

 <p align="center">
<img src="https://i.loli.net/2020/11/16/twlJrqU19b68mus.png" width=400pix>
</p>

<p style="text-align:center;">Fig.1. Simplified principle of our Full-Field OCT system with a common-path imaging interferometer (From the original paper).


A 3D image can be reconstructed by performing a one-dimensional depth scan using the processing interferometer.

The effective imaging range is typically 200um, which is limited by the depth of focus of the probe optics.   The transverse resolution is 3-4um, and the axial resolution is 1-2um.

Flexible method:  using the fiber bundle based probe. 

> The signal-to-noise ratio of the setup is reduced due to cross-talk effects between coupled fiber cores. 

Rigid method: using the Graded-Reflective-Index lens based probe.

> Sensitivity was experimentally evaluated at -80 dB when averaging 20 images during about 1 second, which is enough to get signal from biological tissues. A preliminary in vivo study gave promising results on human skin. 

The system is not suitable for hand-held use; the rigid probe is inaccessible to some areas, such as aero-digestive and gastrointestinal tracts.

#### 021 [In vivo and in vitro diagnostics using Full Field Optical Coherence Tomography](https://www.osapublishing.org/abstract.cfm?URI=BIOMED-2012-BTu3A.95) (2012)

Large areas up to several cm² can be recorded by stitching individual images of typically 1 mm². A 1 cm² image is obtained in less than 4 minutes.

Safety of FFOCT technique on breast tissue was validated by  evaluating the morphological and the immunophenotypic characteristics of the lesions. The information given by a typical FFOCT image, which reveals a refractive-index based contrast is a starting point for an extensive pathology assessment.

In vivo images of healthy skins are obtained using a 3um transverse resolution FFOCT needle probe. It was shown that most of the obtained images were comparable to ex-vivo ones.

Ex-vivo fresh specimens including healthy and pathological brain tissue were imaged to assess to resolution, penetration depth, and clinical relevance of images.

Advantages: do not consume the tissue and do not induce alterations.

Challenges: a number of paraffin-embedded blocks sampled on surgical specimen for morphologic analysis are needed; ancillary techniques by a prior examination of the tissue are not automated and require expertise.

#### 022 [Tissue elasticity imaging using full-field optical coherent tomography](https://www.osapublishing.org/abstract.cfm?uri=BIOMED-2012-BTu3A.75) (2012)

A FFOCT setup includes a static elastography system for multi-parameter images that could complement histopathology diagnostics.  This setup creates various levels of compression.

The static elastography allowed us to produce a map of the elastic properties, and this map highlights changes in the mechanical properties of the tissue.

#### 023 [Multimodal full-field optical coherence tomography on biological tissue: toward all optical digital pathology](https://doi.org/10.1117/12.908459) (2012)

Two imaging modals are combined for obtaining a backscattered endogenous OCT image (FFOCT) and a fluorescence exogenous image (SIM) in parallel.

> OCT images enable to the visualization of morphologic information such as tissue and main microstructures, but fail to identify nuclei due to the nature of the optical contrast used.
>
> SIM provides metabolic information using fluorescence staining of nuclei.

Fluorescent staining of nuclei was obtained using specific fluorescent dyes such as acridine orange.

 <p align="center">
<img src="https://i.loli.net/2020/11/16/hQdPDrRMtcCp5sH.png" width=400pix>
</p>

<p style="text-align:center;">Fig.2. Instrumental setup – combined FFOCT / SIM for fluorescence (From the original paper).


Using the Xenon lamp, integration time was set to 5 ms for the acquisition of FFOCT images, and 35 to 70 ms for the acquisition of fluorescence images for SIM. 

In order to obtain a good signal to noise ratio, several images were averages for each modality: typically 40 images for FFOCT and 5 images for SIM. 

As both types of images can be acquired simultaneously using spectral separation, the average acquisition time for a multimodal image is 1s.

==Result:== the obtained images of skin samples show a significant enhancement of the contrast of nuclei due to fluorescence images, merged with architectural information from FFOCT.

> The visualization of nuclei alone is not useful for the pathologists if not precisely located in the architecture of the tissue.

==To be improved:== the fluorescence light is reduced by the beam splitter (how to optimize fluorescence collection). 

> A separate injection path can be positioned after the beam splitter (before the objective of the sample arm).