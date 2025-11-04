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
    default=true
    src="Objectives.png"
    title="Objective Lenses Expect a Coverslip With Thickness 0.170 mm."
    caption="40X objective lenses showing the 0.17mm coverslip thickness requirement."
    width=500
    >}}

## Why should you care? 
Using the incorrect coverslip for the objective used on the microscope will affect your final image. The following graph shows the degradation of signal intensity for different NA objectives for coverslips of varying thickness. If you are using an objective with an NA of 0.4 (20x objectives and above), you can lose much of your signal. For example, if you are using a 40x Air objective, and using a #1 coverslip you could expect to lose *60-80%* of the fluorescence signal! 
{{< figure
    default=true
    src="IntensityVsThicknessError.png"
    title="Intensity Vs. Error in C/S Thickness"
    caption="source: [*Nikon Microscopy U*](https://www.microscopyu.com/microscopy-basics/coverslip-correction)"
    width=500
    >}}
 

## Imaging Cells
The expectation of the lens manufacturer is that your sample will be ***EXACTLY*** at the surface of the coverslip, if this is not the case, then you will introduce spherical aberration and degrade your image. A common mistake is to use chambered slides instead of chambered coverslips. Chambered slides have chambers that can be removed and a coverglass placed over the chambers for imaging. The problem with this is that the microscope has to image through thick mounting media which often has mismatched refractive index. Most lenses are designed to image at the coverslip, not far from the coverslip. Therefore, resolution may be degraded. High resolution is compromised. Additionally, high NA lenses have minimal free working distance, e.g. a typical 63X/1.4NA lens has a working distance around 140 micrometers. If the distance from the coverslip to the cells on the slide is more than this distance, the lens will touch the top of the coverslip before the cells are in focus. 
{{< figure
    default=true
    src="goodbad.png"
    title="Cells on c/s Vs. Cells on slide"
    width=500
    >}}

