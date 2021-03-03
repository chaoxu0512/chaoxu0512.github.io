---
layout:     post
title:      Note for Chapter2 Basic concepts of medical instrumentation
subtitle:   
date:       2021-03-03
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Paper and Book
    - Medical Instrumentation Application and Design
---

## 2.2 Resistive sensors

**Potentiometers**

![image-20210303085931547](http://imghost.cx0512.com/images/2021/03/02/20210303085938.png)

The fundamental limitation of the resolution is a function of the wire spacing, which may be as small as 20 um. The frictional and inertial components of these potentiometers should be low in order to minimize dynamic distortion of the system.

**Strain gage**

Strain gages can be classified as either unbonded or bonded. <u>Unbonded gages</u> can be used for converting blood pressure to diaphragm movement, to resistance change, then to an electric signal. For the <u>bonded gages</u>, four bonded metal strain gages can be used on cantilever beams to measure bite force in dental research.

<u>Semiconductor strain-gages</u>: high gage factor, but more temperature sensitive and inherently more nonlinear.

<u>Elastic-resistance strain-gages</u>: extensively used in biomedical applications, especially in cardiovascular and respiratory dimensional and plethysmographic (volume-measuring) determinations. These units measure much higher displacements than other gages.

## 2.3 Bridge circuits

The Wheatstone bridge circuit is ideal for measuring small changes in resistance.

![image-20210303092340019](http://imghost.cx0512.com/images/2021/03/02/20210303092340.png)



## 2.4 Inductive sensors

$$
L=n^2G \mu
$$

where n: number of turns of coil, G: geometric form factor, u = effective permeability of the medium.

![image-20210303092928157](http://imghost.cx0512.com/images/2021/03/02/20210303092928.png)



An inductive sensor has an advantage in not being affected by the dielectric properties of its environment. However, it may be affected by external magnetic fields due to the proximity of magnetic materials.

<u>Self-inductance devices</u> have low power requirements and produce large variations in inductance makes them attractive for radiotelemetry applications. The change in inductance for this device is not linearly related to displacement.

Mutual inductance devices can be used in measuring cardiac dimensions, monitoring infant respiration, and ascertaining arterial diameters.

The linear <u>variable differential transformer</u> (LVDI) is widely used in physiological research and clinical medicine to measure pressure, displacement, and force. Linear variable differential transformer characteristics include linearity over a large range, a change of phase by 180° when the core passes through the center position, and saturation on the ends. Sensitivity for LVDTs is much higher than that for strain gages. A disadvantage of the LVDT is that it requires more complex signal processing instrumentation.

## 2.5 Capacitive snesors

The capacitance between two parallel plates of area A separated by distance x is
$$
C=\varepsilon_{0} \varepsilon_{\mathrm{r}} \frac{A}{x}=\frac{1}{2\pi fR}
$$
where $\varepsilon_{0}$ is the dielectric constant of free space and , $\varepsilon_{r}$ is the relative dielectric constant of the insulator (1.0 for air).  

The sensitivity K of a capacitive sensor to changes in plate separation Ax is found by differentiating above equation.
$$
K=\frac{\Delta C}{\Delta x}=-\varepsilon_{0} \varepsilon_{\mathrm{r}} \frac{A}{x^{2}}
$$
The sensitivity increases as the plate separation decreases. The sensor measures the pressure between the foot and the shoe.

## 2.6 Piezoelectric sensors

Piezoelectric sensors are used to measure physiological displacements and record heart sounds. 

Piezoelectric materials generate an electric potential when mechanically strained, and conversely an electric potential can cause physical deformation of the material. 

The principle of operation is that when an asymmetrical crystal lattice is distorted, a charge reorientation takes place, causing a relative displacement of negative and positive charges. The displaced internal charges induce surface charges of opposite polarity on opposite sides of the crystal. Surface charge can be determined by measuring the difference in voltage between electrodes attached to the surfaces.

Piezoelectric sensors are used quite extensively in cardiology for external,(body-surface) and internal (intracardiac) phonoçardiography.
$$
v=\frac{q}{C}= \frac{k f}{C}=\frac{k f x}{\varepsilon_{0} \varepsilon_{\mathrm{r}} A}
$$
where k  is the piezoelectric constant.

![image-20210303100853670](http://imghost.cx0512.com/images/2021/03/02/20210303100853.png)

Above figure shows the voltage-output response of a piezoelectric sensor to a step displacement x. The output decays exponentially because of the finite internal resistance of the piezoelectric material. The simplest approach is to add a parallel capacitor, but it will reduce the sensitivity in the midband frequencies. Another method is to use the charge amplifier. 

## 2.7 Temperature measurements

## 2.8 Thermocouples

Thermoelectric thermometry is based on the discovery of Seebeck in 1821. He observed that an electromotive force (emf) exists across a junction of two dissimilar metals.

<img src="http://imghost.cx0512.com/images/2021/03/02/20210303103957.png" alt="image-20210303103957093" style="zoom:80%;" />

Figure 2.13(a) is a thermocouple circuit with two dissimilar metals, A andB. at two different temperatures, Ti, and T. The net emf at terminals c-d is a function of the difference between the temperatures at the two junctions and the properties of the two metals.

The law of homogeneous circuits states that in a circuit composed of a single homogeneous metal, one cannot maintain an electric current by the application of heat alone.

The law of intermediate metals states that the net emf in a circuit " consisting of an interconnection of a number of unlike metals, maintained at the same temperature, is zero.

The law of intermediate temperatures: emf El is generated when two dissimilar metals have junctions at temperatures T1 and T2 and emf E1 results for temperatures T2 and T3. It follows that an emf El + E2 results at c-d when the junctions are at temperatures T1 and T3.

The advantages of thermocouples: fast response time (time constant as small as 1 ms), small size (down to 12 um diameter), ease of fabrication, and long-term stability. 

Their disadvantages are small output voltage, low sensitivity, and the need for a reference temperature.

 Thermocouples can be made small in size, so they can be inserted into catheters and hypodermic needles.

## 2.9 Thermistors

Thermistors are semiconductors made of ceramic materials that are thermal resistors with a high negative temperature coefficient.

<img src="http://imghost.cx0512.com/images/2021/03/03/20210303110256.png" alt="image-20210303110256908" style="zoom:80%;" />

An application of thermistors is in the clinical measurement of oral temperature. A problem with thermistor neonatal skin surface temperature-monitoring instruments is that the probes fall off.

## 2.10 Radiation thermometry

