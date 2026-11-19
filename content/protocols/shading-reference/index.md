+++
title = 'Whole Slide Shading Correction (Fluorescence)'
layout = "simple"
+++

## Overview

In tiled images, illumination is slightly dimmer at the edges of each field of view (shading, or vignetting). One tile hides it; hundreds of stitched tiles show a visible grid.

**This procedure is for fluorescence slide scans only.** Brightfield scans are corrected automatically, provided your preview frame includes some blank glass (see the [Axioscan page](/systems/axioscanz1)).

{{< figure default=true src="Before.jpg" title="Uncorrected whole-slide image" caption="Tile pattern from uneven illumination." width=500 >}}
{{< figure default=true src="After.jpg" title="Corrected image" caption="After shading correction." width=500 >}}

## How it works

We build a reference for each channel from the **average of your own tiles**, then divide each channel by its reference. This needs ZEN's "Shading Reference from Tile Image" followed by "Shading Correction", then "Add Channels" to reassemble.

> [!IMPORTANT] Requirements
> - A **fluorescence tile image acquired without shading correction** (untick shading correction in the scan profile's *Channels* section).
> - At least **300 tiles in total** (all scenes count).
> - No saturated pixels; use a good fraction of the camera's dynamic range (about 35 % or more).
> - Sparse, evenly distributed signal. In very dense tissue the average contains tissue structure and the correction can create artefacts. Ask the facility about a uniform reference slide.

> [!NOTE] Quantification
> Shading correction changes pixel intensities. Report it in your methods. Keep your original, uncorrected file.

## Step 1: Create a shading reference for each channel

1. Open ZEN and the uncorrected image. Go to **Processing** and choose the method **Shading Reference from Tile Image**.
2. **Input:** your image.
3. **Output:** one output per channel, each set to **Create New Output**.
4. **Parameters:**

| Setting | Value |
|---|---|
| All Scenes | Ticked (if you have several scenes) |
| Adjust per Channel | Unticked |
| Save directly as Shading Reference | **Unticked** |
| Channel-specific | Ticked |
| Autoadjust Intensity | Ticked |
| Multiply factor | 1.0 |
| Apply Gaussian filter | Ticked, sigma about 50 |

5. Click **Apply**. One reference image appears per channel. (A 3-channel image with 775 tiles per channel took about 5.5 minutes.) The images are locked while processing.

The Gaussian filter blurs away detail, leaving the pattern common to all tiles.

{{< figure default=true src="InputOutputParameters.PNG" width=200 >}}
{{< figure default=true src="paramsCloseup.PNG" width=400 >}}
{{< figure default=true src="WorkingApply.PNG" >}}

## Step 2: Correct each channel

The **Shading Correction** method handles one channel at a time, so repeat for each channel.

1. Method: **Shading Correction**.
2. **Input:** your original image, and the reference for the channel you are correcting.
3. **Parameters:**
   - Shading Mode: **Camera Shading** 
   - **Automatic: unticked.** (If ticked, ZEN builds its own reference and the result looks worse.)
   - Adjust per Channel: ticked. Set the current channel to **Process Channel** and the others to **Skip Channel**.
   - Display mode: Multiplicative; offset 0.
4. Click **Apply**. Inspect the result for remaining tile lines.
5. Repeat for each remaining channel, changing both the reference and the processed channel each time.

{{< figure default=true src="CorrInput.PNG" >}}
{{< figure default=true src="CorrDAPIParams.PNG" >}}
{{< figure default=true src="ShadingCorrFITCProcess.PNG" >}}

You can now close the reference images and the original; only the single-channel corrected images are needed.

## Step 3: Combine the channels

**Add Channels** accepts two images at a time.

- 3 channels: add 1 + 2, then add the result to 3.
- 4 channels: add 1 + 2, add 3 + 4, then add the two results.

1. Method: **Add Channels** (no method parameters).
2. Choose the two images in *Image Parameters*, then **Apply**.
3. Repeat until one multichannel image remains.
4. **Save it** (and keep the original). Close the intermediate images without saving.

To extract a scene or channel later, use **Create Image Subset** or **Create Image Subset and Split**.

{{< figure default=true src="AddChannelsImageParams.PNG" >}}
{{< figure default=true src="SecondAddChannelSelectInputDetails.PNG" >}}

{{< columns >}}
{{< figure default=true src="B4.PNG" title="Original" >}}
{{< column >}}
{{< figure default=true src="After.PNG" title="Corrected" >}}
{{< endcolumns >}}

## Common problems

- Result worse than the original: "Automatic" was ticked, or the wrong reference was used for a channel.
- Tile pattern still visible: too few tiles, saturated images, or shading correction was already applied at acquisition.
- Needing the reference later: you can always regenerate it from the original data.
