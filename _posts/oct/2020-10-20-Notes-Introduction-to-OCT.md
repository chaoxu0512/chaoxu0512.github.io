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

$$
\left.I_{o} \sim\left|E_{r}\right|^{2}|+| E_{s}\right|^{2}+2 \cdot E_{r} \cdot E_{s} \cos (2 \cdot k \cdot \Delta L)
$$

$\Delta L$ is the path length difference between the signal and reference arms of the interferometer.

In order to detect optical echoes, a low-coherence (broad bandwidth) light source is required. Low-coherence light can be characterized as having statistical phase discontinuities over a distance known as the coherence length, which is inversely proportional to the frequency bandwidth of the light.

## 1.4 The Development of OCT

### 1.4.1 Early OCT Technology and Systems

**[Optic  nerve head](https://en.wikipedia.org/wiki/Optic_disc)** : also called **optic disc**. It is the point of exit for [ganglion cell](https://en.wikipedia.org/wiki/Retinal_ganglion_cell) [axons](https://en.wikipedia.org/wiki/Axons) leaving the [eye](https://en.wikipedia.org/wiki/Human_eye). Because there are no [rods](https://en.wikipedia.org/wiki/Rod_cell) or [cones](https://en.wikipedia.org/wiki/Cone_cell) overlying the optic disc, it corresponds to a small [blind spot](https://en.wikipedia.org/wiki/Blind_spot_(vision)) in each eye. The ganglion cell axons form the [optic nerve](https://en.wikipedia.org/wiki/Optic_nerve) after they leave the eye. The optic disc represents the beginning of the optic nerve and is the point where the axons of retinal [ganglion](https://en.wikipedia.org/wiki/Ganglion) cells come together. The optic disc is also the entry point for the major blood vessels that supply the [retina](https://en.wikipedia.org/wiki/Retina). The optic disc in a normal human eye carries 1–1.2 million [afferent nerve fibers](https://en.wikipedia.org/wiki/Afferent_nerve_fiber) from the eye towards the brain.

## Reference

[Optical Coherence Tomography-Technology and Applications](https://www.springer.com/gp/book/9783319064185)