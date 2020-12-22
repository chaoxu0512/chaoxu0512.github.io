---
layout:     post
title:      Vis-OCT components part3
subtitle:   
date:       2020-11-26
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Optical Coherence Tomography
---

### 1. Group Shuliang Jiao

Paper: [Visible light OCT-based quantitative imaging of lipofuscin in the retinal pigment epithelium with standard reference targets](https://doi.org/10.1364/boe.9.003768)

[Visible-light optical coherence tomography-based multimodal system for quantitative fundus autofluorescence imaging](https://doi.org/10.1177/1535370218813529)

[Visible-light optical coherence tomography based multimodal retinal imaging for improvement of fluorescent intensity quantification](https://www.osapublishing.org/boe/abstract.cfm?URI=boe-7-9-3220)

Experimental setup:

<p align="center">
<img src="https://i.loli.net/2020/11/26/Eg2sXNxZ4KQqO8u.png" width=600pix>
</p>
<p style="text-align:center;">Fig. 1. Schematic of the simultaneous VIS-OCT and AF imaging system: VIS-OCT (blue), NIR-OCT (red) and A (green). SLD: Superluminescent Diod; SC: Supercontinuum; PMT: Photo Multiplier Tube; SPEC1-2: Spectrometer; ISO: Isolator; M1-3: Reference arm mirrors;IRIS1-2: iris; G1-2: BK7 glass plates; BS: beam splitter; FC1-2: fiber coupler; FP1-6: collimation fiber ports; PC1-2: polarization controller; GM: galvanometer scanner; DM1-2: dichroic mirrors; PH: pinhole, L1-3: lens LPF: long-pass filter; ND filter (OD: 10). </p>

Specific components:

| Item                   | Model                                                        | Note                                        |
| ---------------------- | ------------------------------------------------------------ | ------------------------------------------- |
| Supercontinuum laser   | EXB-6, SuperK EXTREME, NKT Photonics, Denmark                |                                             |
| Band-pass filter       |                                                              | center wavelength: 480 nm, bandwidth: 30 nm |
| Superluminescent diode | SLD-37-HP, Superlum, Russia                                  | center wavelength: 840 nm, bandwidth: 50 nm |
| Dichroic mirror 1      | DMLP505, Thorlabs                                            |                                             |
| Dichroic mirror 2      | NT43-955, Edmund Optics                                      |                                             |
| Telescope system       | Relay lens (f = 75 mm, achromatic) +  ocular lens ([Volk lens, 60D](https://www.volk.com/products/slit-lamp-non-contact-60d)). |                                             |
| Long pass filter       | FGL515M, cut-on wavelength: 515 nm, Thorlabs                 |                                             |
| Data acquisition board | [DAQ, PCIe-6361, National Instruments](https://www.ni.com/en-us/support/model.pcie-6361.html) |                                             |
