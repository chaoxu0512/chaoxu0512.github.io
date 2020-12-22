---
layout:     post
title:      Weekly review for 11.09-11.13
subtitle:   
date:       2020-11-13
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Optical Coherence Tomography
---

#### 1. Dispersion in OCT detection

[phase velocity](https://en.wikipedia.org/wiki/Phase_velocity)

[group velocity](https://en.wikipedia.org/wiki/Group_velocity)

[group velocity dispersion](https://en.wikipedia.org/wiki/Group_velocity_dispersion)

[dispersion (optics)](https://en.wikipedia.org/wiki/Dispersion_(optics))

For the dispersion constant $\beta (\omega )$, the zero-order term is nondispersive, and the first-order and second order can be expressed by phase velocity and group velocity, respectively. 
$$
\begin{aligned}
\beta(\omega) &=\beta\left(\omega_{0}\right)+\beta^{\prime}\left(\omega_{0}\right)\left(\omega-\omega_{0}\right)+\frac{1}{2} \beta^{\prime \prime}\left(\omega_{0}\right)\left(\omega-\mid \omega_{0}\right)^{2}+\ldots \\
&=\frac{\omega_{0}}{v_{p}}+\frac{\omega-\omega_{0}}{v_{g}}+\ldots
\end{aligned}
$$
The correction for the first-order dispersion of coherence length, the A-scan of FD-OCT and TD-OCT detector current is given in terms of phase and group indices of refraction of the sample. ==What about the second-order and higher-order dispersion? How to correct it?==

In practice, the effect of GVD can be reduced by minimizing the GVD mismatch in arm length. For example, the optical fiber lengths in the reference and sample arms should be matched as closely as possible. 

#### 2. Sensitivity falloff in FDOCT

The exponential falloff of sensitivity with depth can be understood as the decreasing visibility of higher fringe frequencies corresponding to large sample depths. The deeper the origin of the backscattered partial wave, the higher the encoding frequency is. The shorter the reference arm, the higher the frequency as well.

#### 3. Phase Shifting method to remove artifacts

 <p align="center">
<img src="https://i.loli.net/2020/11/12/4N26PvyBQfmDxui.png" width=400pix>
</p>

<p style="text-align:center;">Fig.1. FDOCT interferometer with addition of variable round-trip phase delay Φ in the reference arm (From the original book).
> 

#### 4. SNR Analysis for TDOCT and FDOCT

**Sensitivity/signal-to-noise ratio:** the minimum detectable reflected optical power compared with a perfect reflector.

Dynamic range: the range of optical reflectivities observable within within a single acquisition.

Shot-noise is the fundamental limiting noise for optical detection. In OCT detection, design approaches for obtaining shot-noise-limited operation are usually applied. 

The expression for SNR of a TDOCT system is given by,
$$
SN{R_{TDOCT}} = {{\left\langle {{I_D}} \right\rangle _{TDOCT}^2} \over {\sigma _{TDOCT}^2}} = {{{\rho ^2}S_{TDOCT}^2{R_R}{R_S}/2} \over {\rho e{S_{TDOCT}}{R_R}{B_{TDOCT}}}} = {{\rho {S_{TDOCT}}{R_S}} \over {2e{B_{TDOCT}}}}
$$
The SNR is proportional to the detector responsivity $\rho $ and to the power returning from the sample, but is independent of the reference arm power level. 

==What is the impact on SNR when different channels of the spectrometer are used ?==

#### 5. Paper review: FFOCT

From 2004 to 2011, I don’t see much change in the experimental setup of FFOCT. Modifications have been made mainly on:

- the light source: 850 nm LED,  white light source(tungsten halogen, Xenon arc/flash lamp), 1200um (InGaAs CCD is adopted)
- the detector: use one detector/ two detectors (PBS is added);  InGaAs CCD camera was used to make 1200um detection possible.

<p align="center">
<img src="https://i.loli.net/2020/11/06/NG3bzAZqB9vSJcK.png" width=300pix>
</p>
<p style="text-align:center;">Fig.2. Experimental arrangement of the original full- field OCT.</p>

<p align="center">
<img src="https://i.loli.net/2020/11/10/daS6CrxVQc8XKOo.png" width=300pix>
</p>
<p style="text-align:center;">Fig.3. Experimental arrangement of the high speed full- field OCT.</p>

<p align="center">
<img src="https://i.loli.net/2020/11/13/9ipRsA6xQEDt8ko.png" width=300pix>
</p>
<p style="text-align:center;">Fig.4. Experimental arrangement of the ultrafast full- field OCT.</p>

| Instrument                 | Light source                                | Detector                        | Resolution (axial × transverse) in water | Detection sensitivity | Acquisition time per en face image |
| -------------------------- | ------------------------------------------- | ------------------------------- | ---------------------------------------- | --------------------- | ---------------------------------- |
| Original full- field OCT   | Tungsten halogen lamp in Köhler illuminator | High resolution CCD camera      | 0.7 µm × 0.9 µm                          | 90 dB                 | 1 s                                |
| High speed full- field OCT | Fibered xenon arc lamp                      | High speed CMOS camera          | 0.8 µm × 0.9 µm                          | 70 dB                 | 5 ms                               |
| Ultrafast full- field OCT  | Xenon flash lamp in Köhler illuminator      | Two high resolution CCD cameras | 0.8 µm × 0.9 µm                          | 70 dB                 | 10 µs                              |

==It turned out that the third arrangement did not gain its popularity in in vivo use.  Why?==

> The calibration of two cameras is critical to reduce artifacts.
>
> Compensation of polarizing effects in the cornea is difficult.

In 2011, the first in vivo imaging of rat brain was achieve: 250W halogen lamp light source centered at 1100nm with the bandwidth of 200nm. The InGaAs CCD camera was operated at its maximum frequency of 66Hz, and the images are displayed at 33Hz.

<p align="center">
<img src="https://i.loli.net/2020/11/13/FhzU8bEvRNpqiBc.png" width=300pix>
</p>
<p style="text-align:center;">Fig.5. Experimental arrangement of the high-speed full- field OCT for rat brain imaging in vivo.</p>

#### 6. Simulate FD-OCT numerically using MATLAB

```matlab
% Use SI units throughout
lambda0 = 830E-9; % center wavelength of source
dlambda = 20E-9; % FWHM wavelength bandwidth of source
ns = 1.38; % refractive index of sample
ls1 = 100E-6; % location of backscatterer 1
ls2 = 150E-6; % location of backscatterer 2
rs1 = 0.5; % reflectivity of backscatterer 1
rs2 = 0.25; % reflectivity of backscatterer 2
k0 = 2*pi/lambda0; % center propagation constant
delta_k = 2*pi*dlambda/lambda0^2; % FWHM bandwidth of k
sigma_k = delta_k/sqrt(2*log(2)); % standard deviation of k

N = 2^10; % number of sampling points
nsigma = 5; % number of standard deviations to plot on each side of k0

subplot(2, 2 ,1); % Generate the interferogram
k = k0 + sigma_k * linspace(-nsigma,nsigma, N); % array for k
S_k = exp(-(1/2) * (k-k0).^2/sigma_k^2); % Gaussian source PSD
E_s1 = rs1 * exp(i*2*k*ns*ls1); % sample electric field from scatter 1
E_s2 = rs2 * exp(i*2*k*ns*ls2); % sample electric field from scatter 2
I_k1 = S_k .* abs(1 + E_s1 + E_s2).^2; % interferogram (r_R = 1)
plot(k/k0, I_k1/max(I_k1), 'k');
title( 'Interferogram' );
xlabel('Propagation constant k/k_0' );
ylabel( 'Normalized intensity');
axis([0.9 1.1 0 1]);

subplot(2, 2, 2); % Inverse Fourier transform (IFT) of the interferogram
spec1 = abs(fftshift(ifft(I_k1)))/sqrt(N);
dls_prime = 1/(2*nsigma*sigma_k/(2*pi)); % bin= 1/sampling range
ls_prime = dls_prime*(-N/2:N/2-1); % frequency array
plot(ls_prime/(2*ns), spec1/max(spec1), 'k' ); % scale the frequency
title( 'IFT of the interferogram' );
xlabel('Depth ls (m)' );
ylabel( 'Relative reflectivity');
axis([-2*ls2 2*ls2 0 1]);

subplot(2, 2, 3); % IFT of the deconvolved interferogram
spec1_norm = abs(fftshift(ifft(I_k1 ./S_k)))/sqrt(N);
dls_prime = 1/(2*nsigma*sigma_k/(2*pi)); % bin size= 1/sampling range
ls_prime = dls_prime*(-N/2:N/2-1); % frequency array
plot(ls_prime/(2*ns), spec1_norm/max(spec1_norm), 'k' );
title( 'IFT of the deconvolved interferogram' );
xlabel('Depth ls (m)' );
ylabel( 'Relative reflectivity');
axis([-2*ls2 2*ls2 0 1]);

subplot(2, 2, 4); % IFT of the deconvolved differential interferogram
I_k2 = S_k .* abs(-1 + E_s1 + E_s2).^2; % interferogram
delta_I_k = I_k1 - I_k2;
spec2=abs(fftshift(ifft(delta_I_k./S_k)))/sqrt(N);
plot ( ls_prime / ( 2*ns), spec2/max ( spec2), 'k' ) ;
title( 'IFT of the deconvolved differential interferogram');
xlabel( 'Depth ls (m)');
ylabel('Relative reflectivity');
axis([-2*ls2 2*ls2 0 1]);
```

<p align="center">
<img src="https://imghost.cx0512.com/images/2020/11/13/untitled.jpg">
</p>

<p style="text-align:center;">Fig.6.Simulated signal processing in FDOCT with two backscatterers.(From Lihong V. Wang, Biomedical Optics: Principles and Imaging, 2007.)</p>