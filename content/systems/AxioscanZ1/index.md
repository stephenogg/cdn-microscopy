+++
title = 'Axioscan.Z1 Slide Scanner'
layout = 'simple'
+++

## Overview

The Zeiss Axioscan.Z1 automatically scans whole tissue sections on microscope slides in **brightfield** or **fluorescence**. It holds up to [100] standard slides (75 x 25 mm). For each slide it makes a preview, finds the tissue, builds a focus map and scans, all based on a saved **scan profile**.

Best for: histology, whole-section fluorescence, many slides of the same type. Not for: thick or uneven samples, live samples, or very high resolution (use a confocal).

### Specifications

| Item | Specification |
|---|---|
| Fluorescence light source | [Zeiss Colibri 7](EN_product-info_Colibri-7_rel1-0.pdf): 385, 430, 475, 511, 555, 590, 630 nm |
| Filter cubes | [Fs38 (GFP)](https://www.micro-shop.zeiss.com/en/uk/shop/filterAssistant/filtersets/489038-9901-000), [Fs43 (DsRed)](https://www.micro-shop.zeiss.com/en/uk/shop/filterAssistant/filtersets/489043-9901-000), [Fs50 (Cy5)](https://www.micro-shop.zeiss.com/en/uk/shop/filterAssistant/filtersets/488050-9901-000), [Fs96 (DAPI)](https://www.micro-shop.zeiss.com/en/uk/shop/filterAssistant/filtersets/489096-9100-000) |
| Objectives | 2.5x/0.05, Fluar 5x/0.25, Plan-Apo 10x/0.45, 20x/0.8, 40x/0.95 Corr (correction collar) |
| Camera | [Zeiss Axiocam 506 mono](EN_product-info_Axiocam-506_mono.pdf) |
| Software | ZEN 3.1 Slidescan |

## Before you scan: prepare your slides

- Slides must be **clean, dry and fully cured**. No oil, no wet mountant, no dried mountant on the back or edges.
- Coverslip fully attached, no labels or tape overhanging the slide.
- Use **#1.5 coverslips** (see [Coverslip Thickness](/protocols/coverslip-thickness)). For the 40x/0.95 Corr objective, set its correction collar to the coverslip thickness.
- Label written clearly on the frosted end; remove fingerprints.

## How slide scanning differs from confocal

On a confocal you adjust settings while you watch the image. On the Axioscan you decide everything **before** the scan, then the system runs unattended. So you need a good **scan profile**: one per sample type.

The scan profile defines:

1. Contrast method (brightfield or fluorescence)
2. Objective
3. Channels and exposure times
4. Which part of the slide to scan (tissue detection)
5. How to focus (focus map)
6. File naming and storage location

[Application guide (PDF): concepts in whole-slide scanning](axio-scanz1-application-guide.pdf)

## Quick start

{{< timeline >}}

{{< timelineItem icon="1" subheader="Switch on" badge="Start here" >}}
<ul>
<li>Turn on the scanner. There are <a href="IMG_4739.JPG">two power buttons</a>: one on the front and one near the power cable on the left.</li>
<li>The <a href="image1.png">top left corner</a> glows blue while initialising and turns <b>green</b> when ready.</li>
<li>Turn on the computer and wait for the desktop.</li>
<li>Open ZEN (<a href="zenIcon.png">icon</a>), wait for the splash screen, then click <a href="SplashChoice.png"><b>ZEN Slidescan</b></a>. Wait until initialisation finishes.</li>
</ul>
{{< /timelineItem >}}

{{< timelineItem icon="2" subheader="Load your slides" >}}
<ul>
<li>Put the slides into the <a href="loadSlides.png">slide carrier</a>; use the <a href="loadingAid.png">loading aid</a> for many slides. [Orientation: label near the silver clamp; coverslip up. Confirm with one photo.]</li>
<li>Press the open/close button and wait for the door to open.</li>
<li>Pull out any tray, place the carrier(s) on it, <a href="loadSlides.jpg">coverslip up</a>, and close the tray.</li>
<li>Press open/close again. The scanner detects the carriers and a <a href="initialLoad.png">diagram of your slides</a> appears in the Magazine tab.</li>
</ul>
{{< /timelineItem >}}

{{< timelineItem icon="3" subheader="Select a profile and preview" >}}
<ul>
<li>Choose the scan profile (each slide can have its own).</li>
<li>Click <b>Preview scan</b> and wait.</li>
<li>Check that the tissue has been found correctly; correct it if needed.</li>
<li>Choose the storage location (your folder on the Data drive) and a naming rule (commonly date + serial number).</li>
</ul>
{{< /timelineItem >}}

{{< timelineItem icon="4" subheader="Scan" >}}
<ul>
<li>Click <b>Scan</b>. Scans are saved to your chosen folder.</li>
<li>When it finishes, unload your slides.</li>
<li>Copy your data to RDS (see <a href="/protocols/map-network-drive">Map a network drive</a>) and delete it from the computer.</li>
</ul>
{{< /timelineItem >}}

{{< /timeline >}}

## Shading correction

Brightfield scans are shading-corrected automatically (include blank glass inside the preview frame). Fluorescence scans may need correction afterwards: see [Shading Correction](/protocols/shading-reference).

## Creating a scan profile

This is the hardest part of slide scanning. In ZEN 3.1, two wizards help:

- **Smart Profile Selection** (top left, under the profile list): create a profile from scratch.
- A second wizard adapts an existing profile to a new sample.

{{< columns >}}
{{< figure src="SmartProfile.png" nozoom=true caption="Smart Profile wizard" >}}
{{< column >}}
{{< figure src="step1.png" nozoom=true caption="Choose a contrast method" >}}
{{< endcolumns >}}
{{< columns >}}
{{< figure src="step2.png" nozoom=true caption="Choose a sample configuration" >}}
{{< column >}}
{{< figure src="step3.png" nozoom=true caption="Choose a staining intensity" >}}
{{< endcolumns >}}

The workflow is:

1. Name the profile.
2. Set label-image options.
3. Define the preview area.
4. Define tissue detection.
5. Create the focus map.
6. Define scan parameters (objective, channels, exposure).

> [!TIP] Preview frame
> The red frame should cover the **whole slide plus some air** around the edges (this helps automatic shading correction in brightfield) but **not the label**. To limit tissue detection, use the red frame in the *Tissue Detection Settings* section in the next step.

{{< figure src="preview.png" alt="Preview image" caption="Include the entire slide within the red rectangle" default="true" width=400 >}}



## Common mistakes

- Dirty, wet or sticky slides, or labels overhanging.
- Preview frame cutting off tissue, or including the label.
- Exposure set too high (saturation) in fluorescence.
- Fluorescence slides scanned with shading correction already on, then corrected again.
- Leaving data on the computer.

