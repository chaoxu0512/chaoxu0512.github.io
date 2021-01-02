---
layout:     post
title:      Notes 2 - AQ6370D Optical Spectrum Analyzer
subtitle:   
date:       2021-01-02
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Daily Knowledgebase
---

<u>1. ROLL AVG</u>

When a trace is set to ROLL AVG mode, each time measurement is performed the sweep average is taken of the current and past measured data, and the measurement data are updated.

$${W_j}(i) = {W_{j - 1}}(i) \cdot (n - 1)/n + W(i) \cdot 1/n$$

$i = 1,2, \cdots ,N$. 

${W_j}(i)$: Newly displayed waveform

${W_{j - 1}}(i)$: Previously displayed waveform

$W(i)$: Newly obtained waveform

N: Number of sampling points

n: Number of averagings

> The setting values of the NOISE MASK function are not affected by sweep averaging. The noise mask is executed when the results of the sweep average are displayed.
>
> When CHOP MODE in the measurement sensitivity settings is set to SWITCH, two sweepings is one count.

<u>2. Curve Fitting</u>

Use Trace G

<u>3. OFFSET/SPACING</u>

When set to OFFSET, the difference between the moving marker and each fixed marker is displayed. When set to SPACING, the difference between the moving marker and the smallest numbered fixed marker is displayed along with the difference from each of the fixed markers.

<u>4. Power Spectral Density Markers</u>

Power spectral density markers show power values per normalization bandwidth by assuming the marker position on the waveform to be the center.

<u>5. THRESH, ENVELOPE, RMS, PEAK RMS</u>

| Algorithm | Description                                                  |
| --------- | ------------------------------------------------------------ |
| THRESH    | Determines spectrum width from the with between points where the waveform crosses the threshold value. |
| ENVELOPE  | Determines spectrum width from waveform envelope.            |
| RMS       | Determines spectrum width from waveform standard deviation.  |
| PEAK RMS  | Determines spectrum width from waveform mode peak standard deviation. |

<u>6. SMSR</u>

SMSR stands for side-mode suppression ratio. SMSR represents the difference between the mode peak and the side-mode level. It is one of the parameters used to evaluate the performance of DFB-LDs and the like.

<p align="center">
<img src="https://i.loli.net/2021/01/02/X7qnNCOSPWgxcof.png" width=300pix>
</p>
<p style="text-align:center;">Fig.1. Side-mode suppression ratio.</p>

<u>7. THRESH LEVEL & MODE DIFF</u>

**THRESH LEVEL**
This parameter is used to set the threshold level for channel detection.
This setting determines how far down in decibels from the peak level to detect a mode peak as a channel.

**MODE DIFF**
This parameter sets the minimum value for the peak/bottom difference during channel peak detection.
If the waveform peak/bottom difference equals or exceeds this value, it is detected as a mode peak.

<p align="center">
<img src="https://i.loli.net/2021/01/02/3JZrcK6QgPE4iY1.png" width=600pix>
</p>
<p style="text-align:center;">Fig.2. Thresh level and mode diff.</p>