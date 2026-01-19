+++
date = '2026-01-16T10:08:20'
draft = false
layout = "simple"
title = 'Whole Slide Shading Reference Creation'
+++
## Overview
Image artifacts result from the non-uniformity of illumination/excitation across an objective's field of view. This can happen with both brightfield and fluorescence images. These artifacts are generally seen at image edges, due to the nature of the excitation sources and objective lenses. Although they may not be apparent in a single field of view, these aberrations are especially noticeable on tiled images, especially whole slide images, where many hundreds of individual images are stitched together to create montages of entire tissue sections, at the millimeter or centimeter length scale. See both broghtfield and fluorescence examples below.
<br/>
<br/>
This is an image of a kidney stained with H&E (left) and an image of just a blank part of the slide (right):
{{< figure
    default=true
    src="shadingcor1.png"
    title="Brightfield Image Corrupted by Shading"
    caption="Notice the vignetting on the right side of the image."
    width=500
    >}}
<br/>
<br/>
{{< figure
    default=true
    src="shadingcor2.png"
    title="Whole Slide Image Corrupted by Shading"
    caption="Tiling of the microscope lens FOV makes it easy to see the shading."
    width=500
    >}}

## The Goal
The goal in whle slide imaging is to remove the shading to end up with an image like this:
{{< figure
    default=true
    src="shadingcor3.png"
    title="Shading Reference Corrected Whole Slide Image"
    caption="Removal of the obvious tiles by correcting the image with a shading refernce."
    width=500
    >}}

## How To:
Because the shading varies according to the lens and lighting conditions, it's usually best to use the image that you want to correct to generate a shading reference. We're going to use two different programs (Methods) in Zen to correct the image. First we'll use the "Shading Reference from tile Image" to generate a shading reference for each channel from the image we wish to correct. Then, in a second step, we'll apply the "Shading Correction" algorithm to apply the shading references we created in teh previous step to the image, creating a beautifully corrected image that we can use for further image analysis/processing.

> [!TIP]
> Tip Thype.


### Step by Step --- Quickstart --- TL;DR
{{< timeline >}}

{{< timelineItem icon="1" header=" " subheader="Scan slides without applying any correction" badge="start here" >}}
Although it sounds counterintuitive, you want to ensure that the "Scan" step of your scan profile does not have the boxes ticked for Shading Correction in the "Channels" area. Initially we want to generate an image that contains shading. 
{{< /timelineItem >}}
{{< timelineItem icon="2" subheader="setup" >}}
<ul>
    <li>Open the image you want to correct in Zen slidescan.</li>
    <li>Select the "Processing" tab.</li>
    <li>Select the "Shading Reference from Tile Image" Method</li>
</ul>
{{< /timelineItem >}}
{{< timelineItem icon="3" subheader="parameters" >}}

{{< /timelineItem >}}
{{< /timeline >}}