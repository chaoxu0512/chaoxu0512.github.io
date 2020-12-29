---
layout:     post
title:      FFOCT development Part 1
subtitle:   
date:       2020-10-21
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Optical Coherence Tomography
---

## 001 [Full-field optical coherence microscopy](https://www.osapublishing.org/abstract.cfm?URI=ol-23-4-244) (1998)

- Cross-sectional images are not acquired.
- 840nm LED.
- Wide field illumination can be used, and en face images are generated with better lateral resolution. 
- Photoelastic modulator are adopted for path difference modulation.  
- **Multiplexed lock-in detection method (???)**.  
- Axial resolution: 8um; lateral resolution: 2um.  
- Imaging speed and sensitivity are still limited by the camera.

## 002 [High resolution real-time full-field interference microscopy](http://proceedings.spiedigitallibrary.org/proceeding.aspx?articleid=977024) (1999)

- Michelson-type interferometer is adopted in FFOCT. 
- Two identical high NA microscope objective lenses are placed before the sample and reference mirror, respectively (which is actually a Linnik configuration).
- 840nm LED.
- Optical sectioning ability = depth resolution (0.7um) = axial resolution, lateral resolution: 0.3 um when NA = 0.95.  
- Images are produced at the rate of 50 per second with Multiplexed lock-in detection.  
- Photoelastic modulator.
- Imaging speed: 50 images/s.  
- Shorter wavelength and higher NA helps improve axial and lateral resolution.

## 003 [High-resolution full-field optical coherence tomography with a Linnik microscope](https://www.osapublishing.org/ao/abstract.cfm?uri=ao-41-4-805) (2002)

- Linnik interference setup is adopted with high NA (0.85) objectives. 
- Advantages of Linnik configuration: optical path lengths and focusing in both arms can be adjusted independently; improve the spatial resolution; insertion of wave plates into the interferometer arms and use of a polarizing beam splitter are possible only in the Linnik geometry.
- 840nm LED.
- Axial resolution: 1um; transverse resolution: 0.5um.
- Sensitivity: ~80dB at a 1 image/s rate.
- Lock-in detection and photoelastic birefringence modulator.
- Based on a Linnik interferometer (This name is formally used in this paper), optical path lengths and focusing in both arms can be adjusted independently. 
- The full image is recorded in parallel (full field illumination), the time per pixel is equal to the time per image. In other words, **the achievable temporal resolution per pixel is limited to one fourth of the camera frame rate (???).**
- Suitable when sample is immobile when acquiring the images.
- Sensitivity should be improved (reduction of scattering) using a source with a shorter coherence length (white-light source).

## 004 [High resolution thermal light OCT for biological imagery](https://www.osapublishing.org/abstract.cfm?URI=BIO-2002-SuG5) (2002)

- A tungsten halogen light source.
- Axial resolution: 1um; transverse resolution: 1um.

## 005 [Thermal-light full-field optical coherence tomography](https://www.osapublishing.org/abstract.cfm?URI=ol-27-7-530) (2002)

- Thermal white-light source; 100-W tungsten halogen lamp in a Köhler illumination system.
- Parallel detection scheme: CCD camera works at a maximum rate of 200 frames/s, and a piezoelectric transducer supporting the reference mirror creates a sinusoidal phase modulationat the frequency f =50 Hz (exactly a quarter of the image-acquisition rate).
- En face image acquisition speed: 50Hz.
- Axial resolution: ~1.2um; lateral resolution: ~1.3um; NA = 0.3 (Best one at its time).
- Sensitivity of this system: the ratio of the max signal to the min detectable one, ~80dB. 
- Sensitivity is relatively low due to the low brightness of the illumination scheme and the low dynamic range of  CCD sensor. Imaging depth is limited within a few hundred microns.
- Strengths: cheaper light source; high resolution inside biological tissues;  avoids image speckles (stable intensity and spatial incoherence)

## 006 [Full-field birefringence imaging by thermal-light polarization-sensitive optical coherence tomography. I. Theory](https://www.osapublishing.org/abstract.cfm?URI=ao-42-19-3800) (2003)

- The thermal light is adopted as the source. Again, the shortcomings of the light source are mentioned, but the  advantages are also listed (the same as above).
- Resolution in three dimensions: a few micrometers
- Use a Linnik interference microscope and  achromatic quarter-wave plates
- Why polarization-sensitive OCT?  The point defects cause scattering in the optical systems, and thus make them lose efficiency. Birefringence imaging is  a highly efficient way of detecting the change in the polarization of the incident light caused by the scattering defects. A combination of polarization measurement and OCT has been successfully used to image birefringent structures in biological tissues.

## 007 [Full-field birefringence imaging by thermal-light polarization-sensitive optical coherence tomography II Instrument and results](https://www.osapublishing.org/ao/abstract.cfm?uri=ao-42-19-3811) (2003)

- Use a thermal light source
- Axial resolution of 1.5 um, and transverse resolution of 1 um.  
- The maximum sensitivity of the setup, in terms of minimum detectable sample reflectance, was found to be 95 dB (~84 dB for 1-s integration) for an individual image and 61 dB (~50 dB for 1-s integration) for a birefringence measurement.
- The key problem to solve in this paper is to find  a fairly achromatic phase-shift component, which is a critical part of the polarization-sensitive OCT configuration.  Conventional phase-shift components, like Fresnel rhombs and phase-shifting plates, prove to be unsuitable in this situation. The authors chose to use achromatic quarter-wave plates, which are easy for the implementation but also detrimental to the accuracy and sensitivity. 
- The main goal of this paper was to localize the scattering defects more accurately in multilayer optical coatings and therefore to determine the sources of contamination. 

## 008 [Ultrahigh-resolution OCT using white-light interference microscopy](http://proceedings.spiedigitallibrary.org/proceeding.aspx?doi=10.1117/12.477631) (2003)

- Use a white light source by a tungsten halogen lamp, and the bandwidth is 300 nm with its central wavelength of 800 nm. 
- Linnik interferometer setup is adopted, and *en face* images are recorded by a silicon CCD camera.
- Axial resolution of 0.8 um (short coherence length) and transverse resolution of 1.6 um (high numerical aperture, NA = 0.3) are achieved, and the dispersion mismatch is compensated in the reference arm.
- Sensitivity of 90dB is obtained within 4 acquisition time under a nearly shot-noise limited situation.
- Basically, this paper gives a summary of the work achieved before in this group.  The paragraph extracted from the paper properly shows what the FFOCT does:

> Conventional OCT produces cross-sectional (XZ or YZ) images by scanning the beam in one transverse direction (X or Y). In this configuration, low numerical aperture (NA) objectives are used to give a large depth of field. As a consequence, the transverse resolution is limited. En-face (XY) OCT images can also be produced by scanning the beam in two transverse directions (X and Y). In this configuration, high NA can be used to achieve high transverse resolution. Nevertheless, scanning in two directions increases the acquisition time. Our full-field OCT system produces en face tomographic images without scanning.

- The definition of sensitivity is reiterated in this paper (previously proposed [here](https://www.osapublishing.org/ao/abstract.cfm?uri=ao-41-4-805)), and it is expressed in terms of minimal detectable reflectivity:

$$
\left\{ \begin{array}{l}
{R_{\min }} = \frac{{{{\left( {{R_{ref}} + 2{R_{inc}}} \right)}^2}}}{{2N{\xi _{sat}}{R_{ref}}}}\\
Sensitivity = 10\log \left( {{R_{\min }}} \right)
\end{array} \right.
$$

where $R_{ref}$is the reference mirror reflectivity. $R_{inc}$ denotes the amount of the incoherent light, which comes from the setup and the backscattering by biological structures. To reduce the incoherent light, anti-reflection-coated optical components and water-immersion objectives are utilized. In this paper, the full well capacity ${{\xi _{sat}}}$ of CCD pixels equals 100,000. To compensate for this low ${{\xi _{sat}}}$, a large number of images are accumulated. Typically, N = 200 is chosen to obtain an averaged tomographic image within an acquisition time of 4 seconds. Longer time would be incompatible with the acquisition of large stacks of tomographic images. 

## 009 [Full-field optical coherence microscopy](http://proceedings.spiedigitallibrary.org/proceeding.aspx?articleid=1317047) (2004)

