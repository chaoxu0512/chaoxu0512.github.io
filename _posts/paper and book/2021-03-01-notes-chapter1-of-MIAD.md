---
layout:     post
title:      Note for Chapter1 Basic concepts of medical instrumentation
subtitle:   
date:       2021-03-01
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Paper and Book
    - Medical Instrumentation Application and Design
---

## 1.2 Generalized medical instrumentation system

The major difference between medical instrumentation system and conventional systems is that the source of the signals is living tissue or energy applied to living tissue.

Most medically important **measurands**: biopotential, pressure, flow, dimensions (imaging), displacement (velocity, acceleration, and force), impedance, temperature, and chemical concentrations.

## 1.3 Alternative operational modes

Direct-indirect modes

Sampling and continuous modes

Generating and modulating modes

**Generating sensors:** produce signal output from energy taken directly from the measurand; **modulating sensors:** use measurand to alter the flow of energy from an external source in a way that affects the output of the sensor.

Analog and digital modes

Digital modes: greater accuracy, repeatability, reliability, and immunity to noise; periodic calibration is usually not required.

Real-time and delayed-time modes

## 1.4 Medical measurement constraints

Some crucial variables in living systems are inaccessible because the measurands-sensor interface cannot be obtained without damaging the system.

Variables measured from living body are seldom deterministic. The most common method of coping with the variability is to assume empirical statistical and probabilistic distribution functions.

The safe levels of energy of the biomedical measurements are difficult to establish. 

## 1.5 Classification of biomedical instruments

Based on the quantity that is sensed: pressure, flow, temperature.

the principle of transduction: resistive, inductive, capacitive

the organ system: cardiovascular, pulmonary,  nervous

the clinical medicine specialties: pediatrics, obstetrics, cardiology.

## 1.6 Interfering and modifying inputs

**Desired inputs:** the measurands that the instrument is designed to isolate.

**Interfering inputs:** the quantities that inadvertently affect the instrument as a consequence of the principles used to acquired and process the desired inputs.

**Modifying inputs:** undesired quantities that indirectly affect the input by altering the performance of the instrument itself.

## 1.7 Compensation techniques

**Inherent insensitivity**: instrument components are sensitivity only to desired inputs.

**Negative feedback**: less power is needed for the feedback device and input device.

**Signal filtering**

Input filtering blocks interfering and modifying inputs but does not alter the desired inputs.

Electronic filters are often incorporated at some intermediate stage within the instrument .

Output filtering is usually more difficult because desired and undesired output signals are superimposed. 

**Opposing inputs**

An obvious disadvantage of this method is that the amplifier gain has to be adjusted whenever the geometry changes in the system.

## 1.8 Biostatistics

mean, geometric mean, standard mean, coefficient of variation

## 1.9 Generalized static characteristics

Static characteristics describe the performance of instruments for dc or very low frequency inputs.

**Accuracy, precision, resolution, reproducibility, statistical control, static sensitivity**

**Zero shift**

Zero drift has occurred when all output values increase or decrease by the same absolute amount. The following factors can cause zero drift: manufacturing misalignment, variations in ambient temperature, hysteresis, vibration, shock, and sensitivity to forces from undesired directions.

**Sensitivity drift**

When the slope of the calibration curve changes as a result of an interfering and/ or modifying input, a drift in sensitivity results. Sensitivity drift can result from manufacturing tolerances, variations in power supply, nonlinearities, and changes in ambient temperature and pressure 

**Linearity**

high accuracy does not necessarily imply linearity.

**Input ranges**

**Input impedance**

The generalized input impedance Z is the ratio of the phasor equivalent of a steady-state sinusoidal effort input variable (voltage, force, pressure) to the phasor equivalent of a steady-state sinusoidal flow input variable (current, velocity, fow)
$$
P=X_{\mathrm{d} 1} X_{\mathrm{d} 2}=\frac{X_{\mathrm{d} 1}^{2}}{Z_{x}}=Z_{x} X_{\mathrm{d} 2}^{2}
$$

## 1.10 Generalized dynamic characteristics

Dynamic characteristics require the use of differential and/or integral equations to describe the quality of the measurements.

**transfer functions, zero-order instrument, first-order instrument, second-order instrument, time delay**

## 1.11 Design criteria

![image-20210301113807003](http://imghost.cx0512.com/images/2021/03/01/20210301113815.png)

## 1.12 Commercial medical instrumentation development process

## 1.13 Regulation of medical devices

general controls, performance standards, premarketing approval.

