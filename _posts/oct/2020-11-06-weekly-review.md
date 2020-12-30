---
layout:     post
title:      Weekly review for 1101-1106
subtitle:   
date:       2020-11-06
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Optical Coherence Tomography
---

# 1. Prepare for first meeting

## 1.1 Self introduction

## 1.2 Visible light OCT for retinal imaging

| Strength                          | Challenge                       |
| --------------------------------- | ------------------------------- |
| Higher axial resolution (1~2µm)   | Larger  chromatic aberrations   |
| Stronger scattering contrast      | Higher relative intensity noise |
| Stronger oxyhemoglobin absorption | Limited  penetration depth      |
| …                                 | Smaller field of view           |

**Improve the imaging depth** (limited by shorter wavelength of vis-OCT, due to stronger scattering and absorption):

- Supercontinuum sources (500~600nm): larger pulse repetition rate -> lower RIN -> higher sensitivity in deep microstructures;
- •Numerical aperture: larger NA -> smaller speckle size; optical wavelength <-> speckle pattern; 
- •Motion tracking algorithm: reduce motion artifacts; fast and robust in wavelet/ cosine/ space domain.

**Clinical applications**:

- •Detailed visualization of RNFL and GCL, whose thinning is closely related with human glaucoma (high axial resolution);
- •Clear detection of the thickening of Bruch’s membrane, which is the early sign of age-related macular degeneration (deep imaging depth); 
- •Access to oxygen saturation (sO2) or retinal capillary oximetry (strong Hemoglobin absorption).

## 1.3 Full field OCT

**Traditional OCT**: 

A-scan -> B-scan -> large DOF -> low NA (0.1-0.2) -> limited lateral resolution (10-20um) 

**Full field OCT:** 

En face imaging at given depth without scanning -> high NA (0.3-0.5) -> high lateral resolution (1um)

**Experimental setup**

<p align="center">
<img src="https://i.loli.net/2020/11/06/NG3bzAZqB9vSJcK.png" width=200pix>
</p>

<p style="text-align:center;">Fig.1. Experimental arrangement of the full-field OCT technique.(From A. Dubois, A.C. Boccara, Full-Field Optical Coherence Tomography, 2008)</p>

**Light source**: 

- white-light using tungsten halogen lamp

- cheaper

- avoid image speckles (stable intensity, low spatial coherence)
- high resolution inside biological tissues
- low sensitivity (low brightness of illumination and dynamic range of CCD)

**Linnik** **configuration:**

- two identical high NA microscope objectives

- adjust optical path lengths and focusing in both arms independently

**Full field illumination:**

- The full image is recorded in parallel at a given depth, the time per pixel is equal to the time per image.
- It usually takes ∼1 s to record an image, which is much slower than recording a spectrum on a linear array, for example, spectral domain OCT. 

==Limited in vivo studies of full field OCT on eye, skin, brain.== 

**In vivo human corneal imaging**  

<p align="center">
<img src="https://i.loli.net/2020/11/06/Mj29VPdpKY7J8Qx.png" width=300pix>
</p>

<p style="text-align:center;">Fig.2. Schematic illustration of the FFOCT set-up.(From Mazlin, V. et al. Biomed. Opt. Express 9, 557 (2018)).
</p>

- Light source: 850nm LED, Δλ=30nm

- FOV: 1.26mm x 1.26mm with NA = 0.3

- Resolution: 7.7um (axial) x 1.7um (transverse)

- Acquisition time: 3.4ms per en face image

- SNR: 74dB (averaged on 10 images), 60dB (for a single image)

  <p align="center">
  <img src="https://i.loli.net/2020/11/06/8rRWxSgGmDZ9NYb.png" width=300pix>
  </p>

<p style="text-align:center;">Fig.3. In vivo human corneal images of mid and posterior stroma, obtained with FFOCT and CM. (From Mazlin, V. et al. Biomed. Opt. Express 9, 557 (2018)).
</p>

==Less scanning artifacts due to simultaneous pixel acquisition.==

**Challenges to be addressed:** 

- Hard to distinguish superficial, wing, basal epithelial layers

- Impossible to get en face images without cutting through several corneal layers.

- Difficult to acquire volumetric images.

## 1.4 Mendeley and LaTeX

<p align="center">
<img src="https://i.loli.net/2020/11/06/v6wfpCq97EhWbiY.png" width=500pix>
</p>

<p style="text-align:center;">Fig.4. Mendeley, Texlive and Texmaker.
</p>
# 2. Recruitment of Post-doctor researcher

Share the post on xiaomuchong, cc98 of ZJU, WeChat group and circle.

# 3. Paper and book review

## 3.1 Chapter 2 of Fujimoto Book

**Various scanning methods?**

- A-scan, B-scan

- ==C-scan:  en face images at a fixed axial depth position.==
- ==B-scans with lateral or depth priority==
- ==M-scan: repeated A-scans at the same location as a function of time==

**The basic setup of TDOCT, SDOCT and SSOCT? Difference?**

- TDOCT: broadband light source is adopted and the sample arm is fixed, and the reference arm is adjusted. 

- SDOCT: broadband light source is adopted, and the reference arm is fixed at a position approximately corresponding to the position of the sample. The spectral interference of the reference beam and the light backscattered from <u>all depths in the sample</u> is dispersed by a spectrometer and collected simultaneously on an array detector.
- SSOCT: the source has <u>narrow instantaneous linewidth</u> but is rapidly swept in wavelength. The reference arm is also fixed, while the interference fringe is detected on a photoreceiver as a function of time.

**FFOCT in time and frequency domain :** 

> Fourier-domain FFOCT has only been demonstrated using swept sources since a three-dimensional camera would be necessary to obtain the two spatial and one spectral dimensions that would be required for spectrometer-based spectral-domain FFOCT.

See the paper: Považay, Boris, et al. "<u>Full-field time-encoded frequency-domain optical coherence tomography</u>." *Optics Express* 14.17 (2006): 7661-7669.

**Crosstalk artifacts and multiple scattering in FFOCT**

- Originates from ==multiply scattered light== from the scattering samples interferes with singly reflected reference beam.
- There is an coherence-gated imaging depth in the reference. ==What’s the relation between coherence gate and coherence length?==
- In point-scanning OCT, ==the confocal aperture of the single-mode fiber== largely rejects multiply scattered light. However, FFOCT is implemented in free space. 
- Using ==a light source with low spatial coherence== to reduce crosstalk artifacts, for example, thermal sources.

> This creates a spatial coherence gate that serves the same function as the confocal pinhole.

See the paper: Karamata, B., et al. "S<u>patially incoherent illumination as a mechanism for cross-talk suppression in wide-field optical coherence tomography</u>." *Optics letters* 29.7 (2004): 736-738.

- <u>Thermal source</u> is often adopted in FFOCT for low spatial coherence. However, ==it has low brightness, which limits the speed and sensitivity of OCT systems.==
- An alternative is to reduce the spatial coherence of a coherent source, such as a superluminescent diode or femtosecond laser.

**What do the three components (DC, cross-correlation, autocorrelation) of intensity of “spectral interferogram” actually mean in TDOCT?** 
$$
\begin{aligned}
I_{D}(k)=& \frac{\rho}{4}\left[S(k)\left[R_{R}+R_{S 1}+R_{S 2}+\ldots\right]\right] \quad \text { "DC Terms" } \\
&+\frac{\rho}{2}\left[S(k) \sum_{n=1}^{N} \sqrt{R_{R} R_{S n}}\left(\cos \left[2 k\left(z_{R}-z_{S n}\right)\right]\right)\right] \quad \text { "Cross-correlation Terms" } \\
&+\frac{\rho}{4}\left[S(k) \sum_{n \neq m=1}^{N} \sqrt{R_{S n} R_{S m}} \cos \left[2 k\left(z_{S n}-z_{S m}\right]\right] \quad\right. \text { "Auto-correlation Terms" }
\end{aligned}
$$

- The constant or DC component offset to the detector current.  It is independent of path length, and the largest part of the detector current.
- Cross-correlation component for each sample reflector, which is desired component for OCT imaging.  These components are are proportional to the square root of the sample reflectivities, so they are smaller than the DC component.
- Autocorrelation components. They represent interference artifacts between different sample reflectors in typical OCT systems, ==unless  in the common-path system designs, in which the autocorrelation component represents the desired signal==. Usually large reference reflectivity is adopted so that the autocorrelation terms are small compared to the DC and cross-correlation terms.

**Code for demodulation in TDOCT with MATLAB ==(To be verified)==.**

(a) Plot the interference signal versus $\Delta l/{l_c}$, where ${\lambda _0}$=830 nm and $\Delta \lambda $= 60 nm. Estimate the number of periods within the FWHM of the interference envelope. 

(b) Rectify the signal by taking the absolute value of the interference signal. 

(c) Plot the spectral amplitude of the rectified signal.

(d) Filter the rectified signal to produce an envelope.

```matlab
% Use SI units throughout
lambda0 = 830E-9; % center wavelength
dlambda = 60E-9; % bandwidth (delta lambda)
c = 3E8; % speed of light
lc = 4*log(2)/pi*lambda0^2/dlambda % coherence length
Number_of_periods = 0.5*lc/(lambda0/2) % # of periods in FWHM
figure(1);
N = 2^12; % number of sampling points
dl = lc*linspace(-2,2, N); % array for Delta_l
k0 = 2*pi/lambda0; % propagation constant
subplot(2, 2, 1) % interferogram
Iac= exp(-16*log(2)*(dl/lc).^2) .* cos(2*k0 * dl);
plot(dl/lc, Iac, 'k')
title(' (a) Interferogram')
xlabel( '\Deltal/l_c')
ylabel( 'Signal')
axis([-0.6, 0.6, -1, 1])
subplot(2, 2, 2) % rectified interferogram
Irec = abs(Iac);
plot(dl/lc, Irec, 'k')
title(' (b) Rectified interferogram')
xlabel( '\Deltal/l_c')
ylabel( 'Signal')
axis([-0.6, 0.6, -1, 1])
subplot(2, 2, 3) % spectrum of the rectified interferogram
Frec1 = fft(Irec)/sqrt(N);
% order of frequencies: 0,1 ... (N/2-1),-N/2,-(N/2-1) ... -1
Frec2 = fftshift(Frec1);
% shifted order of frequencies: -N/2,-(N/2-1) ... -1, 0,1. .. (N/2-1)
dfreq = 1/(4*lc); % freq bin size= 1/sampling range
freq= dfreq*(-N/2:N/2-1); % frequency array
plot(freq*lambda0, abs(Frec2), 'k')
title('(c) Spectrum of the rectified interferogram')
xlabel('Frequency (1/\lambda_0)')
ylabel( 'Amplitude')
axis([-10, 10, 0, 5])
subplot(2, 2, 4) % envelope
freq_cut = 1/lambda0/2; % cut-off frequency for filtering
i_cut = round(freq_cut/dfreq); % convert freq_cut to an array index
Ffilt = Frec1; % initialize array
Ffilt(i_cut:N-i_cut+1) = 0; % filter
Ifilt = abs(ifft(Ffilt))*sqrt(N); % amplitude of inverse FFT
plot(dl/lc, Ifilt/max(Ifilt), 'k')
Iac_en = exp(-16*log(2)*(dl/lc).^2); % envelope
hold on;
plot (dl( 1: N/32: N) /lc, Iac_en ( 1: N/32: N), 'ko')
hold off;
title('(d) Envelopes')
xlabel( '\Deltal/l_c')
ylabel('Signals')
axis([-0.6, 0.6, -1, 1])
legend( 'Demodulated', 'Original')
```

<p align="center">
<img src="https://i.loli.net/2020/11/06/ZIWxpoU2VhcXeSg.png" width=500pix>
</p>

<p style="text-align:center;">Fig.5. Demodulation in TDOCT. (From Lihong V. Wang, Biomedical Optics: Principles and Imaging, 2007.)
</p>