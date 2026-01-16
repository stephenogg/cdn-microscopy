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
    caption="An H&E stained slide image side by side with the its background image."
    width=500
    >}}



