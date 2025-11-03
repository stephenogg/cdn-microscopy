+++
date = '2025-11-03T15:48:20+01:00'
draft = false
layout = "simple"
title = 'Coverslip Thickness'
+++

## Overview
Many modern microscopy objectives are designed for a #1.5 (or 1.5H) coverslip of 0.17 mm (170 µm) thickness. Thicker or thinner coverslips can cause image blur due to spherical aberration and require using a correction collar on the microscope's objective lens for proper focus. It is crucially important to use the correct coverslip when imaging at the diffraction limit, e.g. with a high numerical aperture lens and sampling that results in pixels , ~100nm in size.

## Common coverslip thicknesses
| Coverslip Number | Thickness (µm)|
|:----------------:|:--------------|
|#0| 85–130|
|#1 |130–160|
|#1.5 |160–190|
|#2  |190–230|
|#3 |240–350|
|#4 |430–650|

## Microscope Objectives 
One of the many pieces of information written onto every objective is the designed (or expected) coverslip thickness. On the following 40x oil immersion objectives from every major vendor, the number 0.17 can be found. This refers to 0.17mm coverslip thickness expected.
{{< figure
    src="Objectives.png"
    caption="40X objective lenses showing the 0.17mm coverslip thickness requirement."
    >}}

## Why should you care? 
Using the incorrect coverslip for the objective used on the microscope will affect your final image. The following graph shows the degradation of signal intensity for different NA objectives for coverslips of varying thickness. The take home message is anything above an NA of 0.4 (20x objectives and above) can lose much of your signal. For example, if you are using a 40x Air objective, and using a #1 coverslip you could expect to lose 60-80% of the fluorescence signal! 
{{< figure
    src="IntensityVsThicknessError.png"
    caption="Graph of the intensity of a point object versus the error in coverslip thickenss."
    >}}
 

