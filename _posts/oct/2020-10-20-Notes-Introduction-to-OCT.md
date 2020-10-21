---
layout:     post
title:      Notes for Chapter 1-Introduction to OCT 
subtitle:   
date:       2020-10-20
author:     Chao Xu
header-style: text 
catalog: true
tags:
    - Optical Coherence Tomography
---

## 1.1 Introduction

**[Raster scanning](https://en.wikipedia.org/wiki/Raster_scan)**: the rectangular pattern of image capture and reconstruction in television. Although often a great deal faster, it is similar in the most general sense to how one's gaze travels when one reads lines of text.

**Optical biopsy**: examination of tissues or liquids from the living body to determine the existence or cause of a disease, in a optical method.

**In situ**: being in the original position

Although histopathology is the gold standard for assessing pathology, it requires excision, fixation, **embedding**, **microtoming**, and **staining** of tissue specimens.

> embedding: fix or set securely or deeply
>
> microtoming: cutting thin slices of something for microscopic examination
>
> staining: the use of a dye to color specimens for microscopic study

**Neovascularization**: Neovascularization is the formation of functional microvascular networks with red blood cell perfusion. Neovascularization differs from angiogenesis in that angiogenesis is mainly characterized by the protrusion and outgrowth of capillary buds and sprouts from pre-existing blood vessels.

> In ophthalmology, choroidal neovascularization is the formation of a microvasculature within the innermost layer of the choroid of the eye. 

**Edema**: swelling from excessive accumulation of serous fluid in tissue.

**Catheter**: a thin flexible tube inserted into the body to permit introduction or withdrawal of fluids or to keep the passageway open.

**laparoscope**: a slender endoscope inserted through an incision in the abdominal wall in order to examine the abdominal organs or to perform minor surgery.

**GI tract**: Gastrointestinal tract, also known as the gut or alimentary canal, is a tube by which bilaterian animals (including humans) transfer food to the digestion organs. 

> In large bilaterians, the gastrointestinal tract generally also has an exit, the anus, by which the animal disposes of solid wastes. Some small bilaterians have no anus and dispose of solid wastes by other means (for example, through the mouth).

## 1.2 OCT and Ultrasound

In order to achieve a 100 $\rm{\mu m}$ resolution for ultrasound imaging, a time resolution of ~100 ns is necessary, which is within the limit of the electronic detection. 

On the other hand, the measurement of distance with a 10$\rm{\mu m}$ resolution for OCT imaging requires  a time resolution of ~30 fs (30$\times 10^{-15}$s). Under this circumstance, high-speed optical imaging, optical correction, or interferometry must be used.  

## 1.3 Measure Optical Echoes

### 1.3.1 Photographing Light in Flight

**[Optical Kerr effect](https://en.wikipedia.org/wiki/Kerr_effect#Optical_Kerr_effect)**: a change in the refractive index of a material in response to an  electric field which is due to the light itself. This causes a variation in index of refraction which is proportional to the local irradiance of the light.

> To achieve high-speed optical Kerr switch, high intensity, short laser pulses are required to induce Kerr effect. It should be a major limitation of this application.

### 1.3.2 Femtosecond Time Domain Measurement

The measurement had a 15 mm axial resolution and was performed using 65 femtosecond duration pulses from a femtosecond dye laser at 625 nm wavelength. Sensitivities of -70 dB or $10^{-7}$ of the incident intensity were achieved. 

> However, these sensitivities were still not high enough to image most biological tissues. Current OCT systems achieve sensitivities 1,000 times higher.

### 1.3.3 Low-Coherence Interferometry

$${I_o} \propto {\left| {{E_r}} \right|^2} + {\left| {{E_s}} \right|^2} + 2 \cdot {E_r} \cdot {E_s}\cos (2 \cdot k \cdot \Delta L)$$

$\Delta L$ is the path length difference between the signal and reference arms of the interferometer.

In order to detect optical echoes, a low-coherence (broad bandwidth) light source is required. Low-coherence light can be characterized as having statistical phase discontinuities over a distance known as the coherence length, which is inversely proportional to the frequency bandwidth of the light.

## 1.4 The Development of OCT

### 1.4.1 Early OCT Technology and Systems

**[Optic  nerve head](https://en.wikipedia.org/wiki/Optic_disc)** : also called **optic disc**. It is the point of exit for **[retinal ganglion cell](https://en.wikipedia.org/wiki/Retinal_ganglion_cell)** **[axons](https://en.wikipedia.org/wiki/Axons)** leaving the eye. Because there are no [rods](https://en.wikipedia.org/wiki/Rod_cell) or [cones](https://en.wikipedia.org/wiki/Cone_cell) overlying the optic disc, it corresponds to a small [blind spot](https://en.wikipedia.org/wiki/Blind_spot_(vision)) in each eye. The ganglion cell axons form the [optic nerve](https://en.wikipedia.org/wiki/Optic_nerve) after they leave the eye. The optic disc represents the beginning of the optic nerve and is the point where the axons of retinal ganglion cells come together. The optic disc is also the entry point for the major blood vessels that supply the **[retina](https://en.wikipedia.org/wiki/Retina)**. The optic disc in a normal human eye carries 1–1.2 million [afferent nerve fibers](https://en.wikipedia.org/wiki/Afferent_nerve_fiber) from the eye towards the brain.

**[Axon](https://en.wikipedia.org/wiki/Axon)**: also called **nerve fiber**, is a long, slender projection of a nerve cell, or neuron, in vertebrates, that typically conducts electrical impulses known as [action potentials](https://en.wikipedia.org/wiki/Action_potential) away from the nerve cell body.

<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/b/b5/Neuron.svg">
    Diagram of neuron (From Wikipedia)
</p>


**[Retinal ganglion cell](https://en.wikipedia.org/wiki/Retinal_ganglion_cell)**: a type of neuron located near the inner surface (the ganglion cell layer) of the **[retina](https://en.wikipedia.org/wiki/Retina)** of the eye. It receives visual information from [photoreceptors](https://en.wikipedia.org/wiki/Photoreceptor_cell) via two intermediate neuron types: [bipolar cells](https://en.wikipedia.org/wiki/Bipolar_cell_of_the_retina) and [retina amacrine cells](https://en.wikipedia.org/wiki/Retina_amacrine_cell). Retina amacrine cells, particularly narrow field cells, are important for creating functional subunits within the ganglion cell layer and making it so that ganglion cells can observe a small dot moving a small distance.

**[Retina](https://en.wikipedia.org/wiki/Retina)**: the vertebrate retina has ten distinct layers. From closest to farthest from the vitreous body:

| Layer                                                        | Note                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [Inner limiting membrane](https://en.wikipedia.org/wiki/Inner_limiting_membrane) | basement membrane                                            |
| [Nerve fibre layer](https://en.wikipedia.org/wiki/Nerve_fiber_layer) | axons of the ganglion cell bodies                            |
| [Ganglion cell layer](https://en.wikipedia.org/wiki/Ganglion_cell_layer) | contains nuclei of ganglion cells, the axons of which become the optic nerve fibres, and some displaced amacrine cells |
| [Inner plexiform layer](https://en.wikipedia.org/wiki/Inner_plexiform_layer) | contains the synapse between the bipolar cell axons and the dendrites of the ganglion and amacrine cells |
| [Inner nuclear layer](https://en.wikipedia.org/wiki/Inner_nuclear_layer) | contains the nuclei and surrounding cell bodies (perikarya) of the amacrine cells, bipolar cells, and [horizontal cells](https://en.wikipedia.org/wiki/Retina_horizontal_cell) |
| [Outer plexiform layer](https://en.wikipedia.org/wiki/Outer_plexiform_layer) | projections of rods and cones ending in the rod spherule and cone pedicle, respectively. These make synapses with dendrites of bipolar cells and horizontal cells. |
| [Outer nuclear layer](https://en.wikipedia.org/wiki/Outer_nuclear_layer) | cell bodies of rods and cones.                               |
| [External limiting membrane](https://en.wikipedia.org/wiki/External_limiting_membrane) | layer that separates the inner segment portions of the photoreceptors from their cell nuclei. |
| Inner segment / outer segment layer                          | inner segments and outer segments of rods and cones. The outer segments contain a highly specialized light-sensing apparatus. |
| [Retinal pigment epithelium](https://en.wikipedia.org/wiki/Retinal_pigment_epithelium) | single layer of cuboidal epithelial cells (with extrusions not shown in diagram). This layer is closest to the choroid, and provides nourishment and supportive functions to the neural retina |

------

**Michelson interferometer with a circulator for dual balanced detection**: dual balanced detection adds the signal form the interference of the sample and reference arms, and subtracts excess noise from the light source to improve efficiency. 

Typical retinal images have signal levels of -50 to -90 dB of the incident intensity.

**Q: The use of relatively longer wavelength light allows it to penetrate into the deeper scattering medium.  Formula? Scattering is used in OCT, but should also be reduced.**

**A**: 

### 1.4.2 Ophthalmic OCT Imaging

## 1.5 Advances in Image Resolution

### 1.5.1 Axial Resolution and Depth of Field

The axial resolution of OCT is determined by the measurement resolution for echo time delay of light.

To derive the formula of axial resolution mathematically,  I turn to the book [Optical Coherence Tomography - Principles and Applications](https://doi.org/10.1016/B978-0-12-133570-0.X5000-8).

To start with time domain OCT, we refer to a monochromatic complex plane wave of this form:

$$E_{s o}=E_{0} e^{-i k(\omega) z}$$

where $k = 2\pi /\lambda $.

When the light changes its polarization states by a mirror or biological tissues, the change can be expressed by multiplying the Jones vector and a 2 x 2 Jones matrix.

<p align="center">
<img src="https://i.loli.net/2020/10/21/IOtQVMJibDSEAq3.png">
    a schematic of time domain OCT.(From Ref [2])
</p>
When the light first emits from  the 50/50 beam splitter, and goes into the sample  and reference arm, respectively,

$${E_{r1}} = \frac{1}{{\sqrt 2 }}{E_{so}}$$

$${E_{s1}} = \frac{i}{{\sqrt 2 }}{E_{so}}$$

As the light propagates, it hits the sample or the mirror, and the light beam is reflected,

$${{E_{r2}} =  - {r_r} \cdot \frac{1}{{\sqrt 2 }}{E_{so}} \cdot {e^{ - ik{l_r}}}}$$

$${{E_{s2}} =  - {r_s} \cdot \frac{i}{{\sqrt 2 }}{E_{so}} \cdot {e^{ - ik{l_s}}}}$$

When the light arrive at the beam splitter for second time (from sample and reference arm), and it goes into the detector arm,

$${{E_{r3}} = \frac{i}{{\sqrt 2 }}{E_{r2}} \cdot {e^{ - ik{l_r}}} =  - i \cdot \frac{{{r_r}}}{2}{E_{so}} \cdot {e^{ - i2k{l_r}}}}$$

$${{E_{s3}} = \frac{1}{{\sqrt 2 }}{E_{s2}} \cdot {e^{ - ik{l_s}}} =  - i \cdot \frac{{{r_s}}}{2}{E_{so}} \cdot {e^{ - i2k{l_s}}}}$$

 The next step is interference in the detector arm, and the field becomes,

$${E_D} = {E_{r3}} + {E_{s3}} = {E_R} \cdot {e^{ - i2k{l_r}}} + {E_S} \cdot {e^{ - i2k{l_s}}}$$

where ${E_R} =  - i \cdot \frac{{{r_r}}}{2}{E_{so}}$, and ${E_S} =  - i \cdot \frac{{{r_s}}}{2}{E_{so}}$.

The irradiance approaching the detector arm is obtained,

$${I_D} =  < {E_D} \cdot E_D^* > $$

$${I_D} =  < {E_R} \cdot E_R^* >  +  < {E_S} \cdot E_S^* >  + {E_R}E_S^* \cdot {e^{ - i2k{l_r} + i2k{l_s}}} + {E_S}E_R^* \cdot {e^{ - i2k{l_s} + i2k{l_r}}}$$

$${I_D} = {I_R} + {I_S} + {\rm{Re(}}\gamma {\left( z \right)_{11}} \cdot \sqrt {{I_R}{I_S}}  \cdot ({e^{i2k\left( {{l_s} - {l_r}} \right)}} + {e^{i2k\left( {{l_r} - {l_s}} \right)}}{\rm{))}}$$

$${I_D} = {I_R} + {I_S} + 2{\rm{Re(}}\gamma {\left( z \right)_{11}} \cdot \sqrt {{I_R}{I_S}}  \cdot \cos (2k\Delta l){\rm{)}}$$

where ${\Delta l}={l_r}-{l_s}$, and ${\gamma {{\left( z \right)}_{11}}}$ is the degree of coherence.

$${\left| {\gamma {{\left( z \right)}_{11}}} \right| = 1,{\rm{coherent - limit}}}$$

$${\left| {\gamma {{\left( z \right)}_{11}}} \right| = 0,{\rm{incoherent - limit}}}$$

$${0 < \left| {\gamma {{\left( z \right)}_{11}}} \right| < 1,{\rm{partial - coherent}}}$$

For TD-OCT, the reference mirror is moving with a velocity of ${v_m} = \frac{{\Delta l}}{t}$, and thus creates a Doppler or frequency shift ${f_D} = \frac{{2{v_m}}}{\lambda }$ in the signal. Therefore, we obtain the irradiance,

$${I_D} = {I_R} + {I_S} + 2{\rm{Re(}}\gamma {\left( z \right)_{11}} \cdot \sqrt {{I_R}{I_S}}  \cdot \cos (2\pi {f_D}t){\rm{)}}$$

## Reference

[1] [Optical Coherence Tomography-Technology and Applications](https://www.springer.com/gp/book/9783319064185)

[2] [Optical Coherence Tomography - Principles and Applications](https://doi.org/10.1016/B978-0-12-133570-0.X5000-8)