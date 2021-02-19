---
layout:     post
title:      Galvanometer scanning systems
subtitle:   
date:       2021-02-19
author:     Chao Xu
header-style: text
hidden: false
mathjax: true
catalog: true
tags:
    - Daily Knowledgebase
---

# 1. Basic tutorial

(1) [How  does a galvanometer confocal scanning system work](https://www.olympus-lifescience.com/en/microscope-resource/primer/java/galvanometerscanning/)

(2) [The principle of a galvanometer](https://www.laserfocusworld.com/optics/article/16567973/product-focus-galvanometer-scanners-what-you-need-to-know-to-buy-a-galvopositioner)

A galvo system consists of three main components: the motor or galvanometer, the mirror or mirrors, and the "servo"—the driver board that controls the system.

(3) [Small Beam Diameter Scanning Galvo Mirror Systems](https://www.thorlabs.com/newgrouppage9.cfm?objectgroup_id=3770) on Thorlabs

Each system includes a single- or dual-axis galvo motor and mirror assembly, associated driver card(s), and driver card heatsink(s). A low noise, linear power supply unit  and motor/mirror assembly heatsink are available separately. Upon initial setup of the system, a function generator or DAQ card will be needed for operating the servo drivers.

| Item #                                          | GVS002                                                       |
| ----------------------------------------------- | ------------------------------------------------------------ |
| Mirror                                          |                                                              |
| Maximum Beam Diameter                           | 5 mm                                                         |
| 2-Axis System Beam Offset                       | 10 mm                                                        |
| Material                                        | Quartz                                                       |
| Coating                                         | Protected Silver                                             |
| Wavelength Range                                | 500 nm to 2.0 µm                                             |
| Damage Threshold                                | 3.0 J/cm2                                                    |
| Parallelism                                     | <3 arcmin                                                    |
| Surface Quality                                 | 40-20 Scratch-Dig                                            |
| Front Surface Flatness (@633 nm)                | λ                                                            |
| Clear Aperture                                  | >90% of Dimension                                            |
| Motor and Position Sensor                       |                                                              |
| Linearity                                       | 0.999                                                        |
| Scale Drift                                     | 40 ppm/°C (Max)                                              |
| Zero Drift                                      | 10 μrad/°C (Max)                                             |
| Repeatability                                   | 15 μrad                                                      |
| Resolution (Mechanical)                         | With GPS011-xx Linear PSU: 0.0008° (15 µrad), With Standard Switch  Mode PSU: 0.004° (70 µrad) |
| Average Current                                 | 1 A                                                          |
| Peak Current                                    | 5 A                                                          |
| Maximum Scan Angle(Mechanical Angle)            | ±12.5° (Input Scale Factor 0.8 V per degree)                 |
| Motor Weight(With Cables, Without  Brackets)    | 50 g                                                         |
| Operating Temperature Range                     | 0 to 40 °C                                                   |
| Optical Position Sensor Output Range            | 40 to 80 µA                                                  |
| Drive Electronics                               |                                                              |
| Full Scale Bandwidth                            | DC to 100 Hz Square Wave, DC to 250 Hz Sine Wave, DC to 175 Hz Triangular Wave, DC to 175 Hz Sawtooth |
| Small Angle (±0.2°) Bandwidth                   | DC to 1 kHz                                                  |
| Small Angle Step Responseb                      | 300 µs                                                       |
| Power Supply                                    | ±15 to ±18 VDC,(1.25 A rms, 5 A peak Max)                    |
| Analog Signal Input Resistance                  | 20 kΩ ± 1% (Differential Input)                              |
| Position Signal Output Resistance               | 1 kΩ ± 1%                                                    |
| Analog Position Signal Input Range              | ±10 V                                                        |
| Mechanical Position Signal Input Scale  Factor  | Switchable: 1.0 V, 0.8 V or 0.5 V per degree                 |
| Mechanical Position Signal Output Scale  Factor | 0.5 V per degree                                             |
| Operating Temperature Range                     | 0 to 40 °C                                                   |
| Servo Board Size (W x D x H)                    | 85 mm x 74 mm x 44 mm (3.35" x 2.9" x  1.73")                |

**System Operation**
The servo driver must be connected to <u>a DC power supply</u>, <u>the galvo motor</u>, and <u>an input voltage source</u> (<u>the monitoring connection</u> is optional). 

For continuous scanning applications, a function generator with a square or sine wave output is sufficient for scanning the galvo mirror over its entire range. For more complex scanning patterns, a programmable voltage source such as a DAQ card can be used. Please note that these systems do not include a function generator or a DAQ card. 

The ratio between the input voltage and mirror position is switchable, either 0.5, 0.8 or 1. When set to 0.8, the ±10 V input will rotate the mirror over its full range of ±12.5°. The control circuit also provides monitoring outputs that allow the user to track the position of the mirror. In addition, voltages proportional to the drive current being supplied to the motor and the difference between the command position and the actual position of the mirror are supplied by the control circuit.

**Closed-Loop Mirror Positioning**
The angular orientation (position) of the mirror is optically encoded using an array of photocells and a light source, both of which are integrated into the interior of the galvanometer housing. Each mirror orientation corresponds to a unique ratio of signals from the photodiodes, which allows for the closed-loop operation of the galvo mirror system.

The systems can be driven to scan their full mechanical range of ±12.5° at a frequency of 100 Hz when using a square wave control input voltage or at 250 Hz when using a sine wave. For a single small-angle step of 0.2°, it takes the mirror 300 μs to come to rest at the command position. The scan frequency range is DC to 1 kHz and the angular resolution is 0.0008° (15 μrad).