---
layout:     post
title:      Notes for Chapter 1-Introduction to OCT 
subtitle:   
date:       2020-10-20
author:     Chao Xu
header-style: text
hidden: true 
mathjax: true
catalog: true
tags:
    - Optical Coherence Tomography
---

This is the note for the book `Optical Coherence Tomography-Technology and Applications` [[1]](https://www.springer.com/gp/book/9783319064185).

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

$$
{I_o} \propto {\left| {{E_r}} \right|^2} + {\left| {{E_s}} \right|^2} + 2 \cdot {E_r} \cdot {E_s}\cos (2 \cdot k \cdot \Delta L)
$$

$\Delta L$ is the path length difference between the signal and reference arms of the interferometer.

In order to detect optical echoes, a low-coherence (broad bandwidth) light source is required. Low-coherence light can be characterized as having statistical phase discontinuities over a distance known as the coherence length, which is inversely proportional to the frequency bandwidth of the light.

## 1.4 The Development of OCT

### 1.4.1 Early OCT Technology and Systems

**[Optic  nerve head](https://en.wikipedia.org/wiki/Optic_disc)** : also called **optic disc**. It is the point of exit for **[retinal ganglion cell](https://en.wikipedia.org/wiki/Retinal_ganglion_cell)** **[axons](https://en.wikipedia.org/wiki/Axons)** leaving the eye. Because there are no [rods](https://en.wikipedia.org/wiki/Rod_cell) or [cones](https://en.wikipedia.org/wiki/Cone_cell) overlying the optic disc, it corresponds to a small [blind spot](https://en.wikipedia.org/wiki/Blind_spot_(vision)) in each eye. The ganglion cell axons form the [optic nerve](https://en.wikipedia.org/wiki/Optic_nerve) after they leave the eye. The optic disc represents the beginning of the optic nerve and is the point where the axons of retinal ganglion cells come together. The optic disc is also the entry point for the major blood vessels that supply the **[retina](https://en.wikipedia.org/wiki/Retina)**. The optic disc in a normal human eye carries 1–1.2 million [afferent nerve fibers](https://en.wikipedia.org/wiki/Afferent_nerve_fiber) from the eye towards the brain.

**[Axon](https://en.wikipedia.org/wiki/Axon)**: also called **nerve fiber**, is a long, slender projection of a nerve cell, or neuron, in vertebrates, that typically conducts electrical impulses known as [action potentials](https://en.wikipedia.org/wiki/Action_potential) away from the nerve cell body.

<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/b/b5/Neuron.svg">
</p>

<p style="text-align:center;">Diagram of neuron (From Wikipedia).</p>

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

It was mentioned that early OCT instruments had an axial resolution of 10 um and an imaging speed of 100 A-scans/s in the 1990s.

In 2002, the Stratus OCT achieved the similar axial resolution of 10 um, but with a faster speed of 400 A-scans/s. 

In mid-2000s, imaging speed is greatly improved due to the introduction of Spectral/Fourier domain OCT.

### 1.4.3 Catheter and Endoscopic OCT Imaging Technology

Two forms of imaging are applied to achieve catheter  endoscopic imaging: (1) a transverse image in the luminal structures us generated by scanning the OCT beam with a rotating torque table; (2) the image can also be obtained by a push-pull movement of the torque cable in a longitudinal plane.

### 1.4.4 Intravascular OCT Imaging

In 1999, Fujimoto et al. performed an intravascular OCT animal imaging on a rabbit [[2]](https://heart.bmj.com/content/82/2/128.short). In this time domain system, an axial resolution of 10 um was achieved at 1,280 nm wavelength using a broadband femtosecond laser. The diameter of the adopted optical catheter was 2.9 French or ~1 mm. The images of 512 axial pixels were acquired at the speed of 4 frames/s. 

Below is the brief history of  intravascular OCT imaging [[1]](https://www.springer.com/gp/book/9783319064185):

The commercial development of intravascular OCT was performed by an MIT startup in 1998. 

The first commercial intravascular OCT instrument generated images with 200 A-scans/frame at 15 frames/s and was introduced in Europe in 2004. 

A higher performance system with 240 A-scan per frame at 20 frames/s was introduced in 2007. 

A system based on swept source/Fourier domain detection achieved 500 A-scans per frame at 100 frames per second, and FDA approval was obtained in 2010.

### 1.4.5 Endoscopic OCT and Cancer Detection

Early endoscopic imaging devices used a 1.5–2 mm diameter probe which adopted a miniature magnetic scanner to image in the forward direction.

About the contrast of OCT imaging, here is a paragraph abstracted from the book  [[1]](https://www.springer.com/gp/book/9783319064185):

> OCT imaging relies on intrinsic contrast produced by variations in scattering properties of different tissue structures. On the positive side, OCT enables real time imaging of tissue pathology in situ, without the need for excision and processing as in conventional biopsy and histopathology. When used to guide biopsy, it is not necessary for OCT to perform at the level required for diagnosis, but it must have sufficient sensitivity to detect pathology and improve the sensitivity of excisional biopsy by reducing sampling errors.

## 1.5 Advances in Image Resolution

### 1.5.1 Axial Resolution and Depth of Field

The axial resolution of OCT is determined by the measurement resolution for echo time delay of light, and the formula is given as below,
$$
\Delta z = \frac{{2\ln 2}}{\pi } \cdot \frac{{{\lambda ^2}}}{{\Delta \lambda }}
$$
To derive the formula of axial resolution mathematically,  I first turned to Chapter 5 of the book `Optical Coherence Tomography - Principles and Applications` [[3]](https://www.sciencedirect.com/book/9780121335700/optical-coherence-tomography). The derivation of Time-domain OCT axial resolution can be seen in the [v1](.\2020-10-23-derivation-of-tdoct-axial-resolution-v1.md). However, it turns out that the book is not as good as I thought before. I found many mistakes, for example, math forms, lack of coefficients.

Therefore, I found another book `Biomedical Optics: Principles and Imaging` [[4]](https://onlinelibrary.wiley.com/doi/book/10.1002/9780470177013), and it’s indeed a good one. The derivation of axial resolution for time domain OCT is accurate. I follow the instructions step by step, and some notes in the [v2](.\2020-10-24-derivation-of-tdoct-axial-resolution-v2.md).

The transverse resolution is,
$$
\Delta x = \frac{{4\lambda }}{\pi } \cdot \frac{f}{d} \approx \frac{{2\lambda }}{{\pi  \cdot {\rm{NA}}}}
$$
Here $\Delta x$ denotes the diffraction limited minimum spot size, which means it is defined from the perspective of diameter. 

The depth of field or confocal parameter b, which is 2$z_R$ or two times the Rayleigh range, is given,
$$
b = 2{z_R} = 2\frac{{\pi {{\left( {\Delta x/2} \right)}^2}}}{\lambda } = \frac{{\pi  \cdot \Delta {x^2}}}{{2\lambda }}
$$
The coefficient of the formula is little different from that in the original book.

### 1.5.2 Optical Coherence Microscopy and En Face OCT

## Reference

[1] Drexler, Wolfgang, and James G. Fujimoto, eds. *Optical coherence tomography: technology and applications*. Springer Science & Business Media, 2008.

[2] Fujimoto, J. G., et al. "High resolution in vivo intra-arterial imaging with optical coherence tomography." *Heart* 82.2 (1999): 128-133.

[3] Brezinski, Mark E. *Optical coherence tomography: principles and applications*. Elsevier, 2006.

[4] Wang, Lihong V., and Hsin-I. Wu. *Biomedical optics: principles and imaging*. John Wiley & Sons, 2012.

