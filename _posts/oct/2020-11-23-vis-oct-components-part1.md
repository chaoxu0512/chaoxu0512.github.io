---
layout:     post
title:      Vis-OCT components part 1
subtitle:   
date:       2020-11-23
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Optical Coherence Tomography
---

### 1. Group Hao F. Zhang

Paper: [Longitudinal deep-brain imaging in mouse using visible-light optical coherence tomography through chronic microprism cranial window](https://doi.org/10.1364/BOE.10.005235)

Experimental setup:

<p align="center">
<img src="https://imghost.cx0512.com/images/2020/11/23/image.png" width=600pix>
</p>
<p style="text-align:center;">Fig.1. Schematic of the experimental vis-OCT system. C: collimator; CL: camera lens; DC: dispersion compensation; FC: fiber coupler; G: grating; GS: galvanometer scanners; LC: line camera; M: mirror; SC: supercontinuum; SL: scan lens; SM: spectrometer.</p>

Specific components:

| Item                      | Model                                                        | Note                                |
| ------------------------- | ------------------------------------------------------------ | ----------------------------------- |
| Light source              | SuperK EXTREME EXW-6, NKT Photonics                          |                                     |
| Short pass filter         | Semrock FF02-694                                             |                                     |
| 30:70 fiber coupler       | [Nufern 460-HP, Gould Fiber Optics](https://gouldfo.com/products/couplers-splitters/single-mode/ultra-band-and-wideband/) |                                     |
| Galvanometer scan mirrors | [QS-7, ](https://www.nutfieldtech.com/qs-7-opd-galvanometer-scanner/)[Nutfield](https://www.nutfieldtech.com/qs-7-opd-galvanometer-scanner/)[ Technology](https://www.nutfieldtech.com/qs-7-opd-galvanometer-scanner/) | a pair                              |
| Scan lens                 | [LSM03-VIS, Thorlabs](https://www.thorlabs.com/thorproduct.cfm?partnumber=LSM03-VIS) | f =39mm                             |
| Spectrometer              |                                                              | spectral range from 510nm to 614 nm |

### 2. Group Yali Jia

Paper: [Angiographic and structural imaging using high axial resolution fiber-based visible-light OCT](https://doi.org/10.1364/BOE.8.004595)

Experimental setup:

<p align="center">
<img src="https://imghost.cx0512.com/images/2020/11/23/image697148ce1f20fc98.png" width=600pix>
</p>
<p style="text-align:center;">Fig.2. Schematic of the visible light optical coherence tomography (vis-OCT) system for rat retina imaging. L1, L2: Lens.</p>

Specific components:

| Item                                       | Model                                                        | Note                                               |
| ------------------------------------------ | ------------------------------------------------------------ | -------------------------------------------------- |
| Illumination light source                  | Super-K EXTREME, NKT Photonics                               | Illumination  range: 1200 nm                       |
| Calibration light source                   | NE-1, Ocean Optics                                           |                                                    |
| Short- pass and long-pass edge filter pair | BrightLine, Semrock                                          | Cutoffs at 496 nm and 630 nm                       |
| 10:90 fiber coupler                        | [TW560R2F2, Thorlabs ](https://www.thorlabs.com/thorproduct.cfm?partnumber=TW560R2F2) |                                                    |
| Reflective collimator                      | [RC08FC-P01, Thorlabs](https://www.thorlabs.com/thorproduct.cfm?partnumber=RC08FC-P01) | Achromatic, protected silver reflective collimator |
| A pair of triangular glass blocks          | BK7                                                          | Dispersion adaptation by the thickness of glass    |
| Neutral density filter                     | NDC-100C-4M, Thorlabs                                        | Prevent saturation of CMOS                         |
| Protected silver mirror                    | PF-10-03-P01, Thorlabs                                       | Reflect the light back into the coupler.           |
| Galvanometer scan mirrors                  | [GVS002, Thorlabs](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_id=3770) |                                                    |
| Telescope system                           | Objective lens (f = 75 mm) + ocular lens (f = 15 mm)         | direct the beam to the sample                      |
| Scan lens                                  | [LSM03-VIS, Thorlabs](https://www.thorlabs.com/thorproduct.cfm?partnumber=LSM03-VIS) | focus the scanning beam on the sample              |
| Transmission grating                       | Wasatch Photonics                                            | spatially dispersion, 1800 lines/mm                |
| Line scan camera                           | spl2048-140km, Basler                                        |                                                    |
| Data acquisition card                      | USB-6353, National Instruments                               |                                                    |

### 3. Group Vivek J. Srinivasan

Paper: [Structural and functional human retinal imaging with a fiber-based visible light OCT ophthalmoscope](https://doi.org/10.1364/boe.8.000323)

[Ultrahigh resolution retinal imaging by visible light OCT with longitudinal achromatization](https://doi.org/10.1364/boe.9.001477)

Experimental setup:

<p align="center">
<img src="https://imghost.cx0512.com/images/2020/11/23/imagea6ef29e26d739256.png" width=600pix>
</p>
<p style="text-align:center;">Fig. 3. (A) Fiber-based visible light spectral / Fourier domain OCT system for imaging the human retina (M: mirror, SPF: short pass filter, LPF: long pass filter, AL: achromatizing lens, RC: reflective collimator, L: lens, FL: focusing lens, DG: diffraction grating, LSC: line-scan camera, NDF: neutral density filter, DM: dichroic mirror). (B) Zero-power triplet achromatizing lens (AL) used in the sample arm.</p>

Specific components:

| Item                                       | Model                                                        | Note                                                         |
| ------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Light source                               | EXU3, NKT Photonics A/S, Birkerød, Denmark                   | 156 MHz repetition rate                                      |
| Short and long pass filter                 |                                                              | a range of 475 - 650 nm                                      |
| 10:90 fiber coupler                        | [TW560R2A2, Thorlabs ](https://www.thorlabs.com/thorproduct.cfm?partnumber=TW560R2A2) | single-mode 460-HP fiber, maximize the coupling of backscattered light from the sample to the detection port |
| Reflective collimator                      | [RC02APC-P01, Thorlabs](https://www.thorlabs.com/thorproduct.cfm?partnumber=RC02APC-P01) | 90° off-axis parabolic mirror, protected silver reflective collimator, 7 mm focal length, achromatic |
| Achromatizing lens                         |                                                              | zero-power triplet                                           |
| Galvanometer scan mirrors                  | CTI 6210H, Cambridge Technology                              |                                                              |
| quasi-telecentric beam expander/compressor | Scan lens (f = 37.5 mm) + ocular lens (f = 50 mm)            | Both achromatic doublet pairs                                |
| Dichroic mirror                            |                                                              | Direct the red LED light for eye fixation                    |
| Neutral density filter                     |                                                              | adjust the reference power                                   |
| Water cell                                 |                                                              | 20 mm water, dispersion balancing during retinal imaging.    |
| Volume transmission grating                | Wasatch Photonics                                            | 1800 lines per millimeter                                    |
| Line-scan camera                           | Basler SPL 4096-140km                                        |                                                              |

In a recent [paper](https://doi.org/10.1364/boe.10.002918), a new method was proposed that utilizes a grating light valve spatial light modulator ([GLV-SLM, F1088, Silicon Light Machines, LLC](http://www.siliconlight.com/en/products/module.html)) to rapidly and precisely shape the supercontinuum source.

### 4. Some components not found in paper

| Item             | Model                                                        | Note                                                         |
| ---------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Fiber collimator | [C80APC-A, Thorlabs ](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_id=11585) | 80 mm Focal Length, AR Coated for 400 - 650 nm, Achromatic Fiber |
|                  |                                                              |                                                              |
|                  |                                                              |                                                              |
|                  |                                                              |                                                              |
|                  |                                                              |                                                              |