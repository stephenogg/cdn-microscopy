+++
title = 'Abberior Mirava Polyscope (STED)'
layout = 'simple'
+++

## Overview

The [Abberior MIRAVA POLYSCOPE](https://abberior.rocks/superresolution-confocal-systems/mirava-polyscope/) combines confocal and STED imaging to go beyond the diffraction limit.

{{< youtubeLite id="Hbceyx8xY2I" label="Mirava STED Introduction" title="An Introduction to the Mirava Polyscope" >}}

Our system does **not** have the MINFLUX module, MATRIX array detector or TIMEBOW FLIM option.

**Offline software:** [download](https://github.com/stephenogg/cdn-microscopy/releases/tag/0.0.1) the viewer for your own computer (macOS .dmg or Windows .msi).

## Safety

- The system contains a **Class 4** depletion laser (775 nm). Never remove covers, and never look into the beam path.
- Do not open the sample enclosure during scanning unless the interlock instructions say so.
- Only STED-suitable, fixed samples are allowed. Live-cell STED must be agreed with the facility first.

## Specifications

| Item | Specification |
|---|---|
| Stand | Olympus IX83, motorised, inverted |
| Widefield (finding samples) | coolLED excitation, quad-band filter (DAPI/FITC/Cy3/Cy5) |
| Stage | Motorised XY; 200 µm Z range |
| Excitation lasers | 405, 488, 561, 640 nm |
| Scanner | Point scanner, up to 2.6 kHz line frequency |
| Objective | UPLXAPO 60x/1.42 oil (*0.15 mm working distance*) |
| Depletion laser | 775 nm (2D and 3D STED) |
| Resolution (vendor best case) | Confocal about 250 nm lateral, 750 nm axial; 2D STED about 30 nm; 3D STED about 80 nm isotropic |
| Detectors | 3 APDs (65% QE, dark counts < 250 Hz) |
| Other | RAYSHAPE adaptive optics; TRUESHARP deconvolution; adaptive illumination (RESCue, DyMIN) |

Resolution depends heavily on your sample, label and settings. Real values are usually worse than the vendor figures.

## Prepare your sample

### STED quality depends on the sample as much as on the microscope.

- **Coverslip:** #1.5H, sample against the coverslip (see [Coverslip Thickness](/protocols/coverslip-thickness)).
- **Fixation:** preserve structure and antigen accessibility; avoid autofluorescent fixatives.
- **Labelling:** dense, specific labelling; small labels where possible (large probes limit resolution).
- **Dyes:** use bright, photostable dyes proven at 775 nm, such as Abberior STAR, ATTO or selected Alexa Fluor dyes.
- **Mounting:** use a mounting medium with refractive index matched to the oil objective, and allow it to cure.
- **Controls:** prepare a single-label and a no-primary control.

More detail: [Sample prep PDF](samplePrep.pdf).

> Even the best STED system cannot recover information lost through poor preservation, weak labelling or bleaching.

## Quick start

Full manual: [LiGHTBOX manual (PDF)](LiGHTBOXmanual.pdf).

{{< timeline >}}

{{% timelineItem icon="1" header=" " subheader="Switch on" badge="Start here" %}}

- The computer is normally already on.
- Switch on the IX83 stand controller and the coolLED controller ( yellow labels <span style="color: black; background-color: yellow;">1</span> & <span style="color: black; background-color: yellow;">2</span>), then the stand touch panel (<span style="color: black; background-color: yellow;">3</span>). Wait until it has initialised.
- Log in with your King's credentials and open **LiGHTBOX**. Starting the software powers up the system.
- **Wait 30 minutes** for the STED laser to warm up before imaging.
- Hover over the status indicator (top right of the Welcome screen) to check that all modules are ready.

{{% /timelineItem %}}

{{% timelineItem icon="2" header=" " subheader="Auto-alignment" badge="First user of the day" %}}

- Only the first user of the day does this, after the 30-minute warm-up.
- Get the auto-alignment slide from the facility manager and mount it.
- Choose **Measurement > Auto alignment** and let it finish (2–5 minutes).
- Return the slide afterwards.

{{% /timelineItem %}}

{{% timelineItem icon="3" header=" " subheader="Focus and find your field" badge="Widefield" %}}

- Add oil to the objective (max 2 drops), then mount your sample.
- On the touch panel choose **FL** (fluorescence) and switch the LED on, then select the excitation wavelength. For brightfield choose **BF** and set lamp brightness in the **DIA** pane.
- Focus: turning the focus wheel **clockwise lowers** the objective, away from the sample.
- Stage: top dial moves X, bottom dial moves Y, third dial is unused. **+/-** change stage speed. Press the green LED on the stage to release it for manual movement; press it again to lock it.

{{% /timelineItem %}}

{{% timelineItem icon="4" header=" " subheader="Set where to save" badge="Before you acquire" %}}

- In the Welcome hamburger menu choose **Change default save location**.
- Use the **D:** drive, in a folder named after you (create it if needed). Do not save to the default folder.

{{% /timelineItem %}}

{{% timelineItem icon="5" header=" " subheader="Choose your dyes" badge="Acquisition setup" %}}

- Select **New Sample**, then drag your dyes from the list on the left to the right.
- Optional: add a sample name, dye details and notes; choose colour maps.
- Press **START**.

{{% /timelineItem %}}

{{% timelineItem icon="6" header=" " subheader="Preview" badge="Preview" %}}

- **PREVIEW** scans continuously. Move the sample by dragging the image or with the stage controller.
- Focus with the Z-drive wheel (moves the lens) or the mouse wheel over the image (moves the piezo).
- **PREVIEW** again stops at the end of the current frame; **STOP** stops immediately.

{{% /timelineItem %}}

{{% timelineItem icon="7" header=" " subheader="Overview" badge="Optional" %}}

- Click **EXPLORE**, set the number of fields of view, then **NEW OVERVIEW** (spiral scan from the current position).
- Use about 10% overlap for tiling.

{{% /timelineItem %}}

{{% timelineItem icon="8" header=" " subheader="Organise images" badge="Image tree" %}}

- All images from the session appear in the Image Tree. Add folders with the plus icon; rename by double-clicking; drag items between folders.
> [!CAUTION] **Delete is immediate and cannot be undone.**

{{% /timelineItem %}}

{{% timelineItem icon="9" header=" " subheader="Acquire a region" badge="Acquisition" %}}

- Choose the **Draw image region** tool (shown in orange when active) and draw an ROI on an overview or image. Hover over a corner to rotate it.
- Large ROIs are tiled automatically.
- **PREVIEW** scans the ROI continuously; **ACQUIRE** records one scan.

{{% /timelineItem %}}

{{% timelineItem icon="10" header=" " subheader="Acquisition settings" badge="Confocal" %}}
{{< katex >}}
- Settings are in the **Acquisition** menu in the Scanning tab.
- **Avoid detector saturation.** The APDs saturate above 10,000,000 counts per second; counts become non-linear well before this [recommended maximum – confirm]. Check that the maximum counts per pixel divided by the pixel dwell time stays below the limit. Example: with a 5 µs dwell time, 50 counts per pixel gives \(\dfrac{50}{5\times10^{-6}} = 10{,}000{,}000\) counts per second, which is already the limit.
- Adjust laser power with the mouse wheel (1% steps; <kbd>Alt</kbd> = 0.1%, <kbd>Shift</kbd> = 10%).
- For more signal, use line accumulations rather than more power.
- Confocal pixel size: **80 nm** for full resolution with this lens.

{{% /timelineItem %}}

{{% timelineItem icon="11" header=" " subheader="Acquisition settings" badge="STED" %}}

- Add a STED channel with the plus symbol under **STED**; a donut icon appears below the confocal channel.
- Set the STED laser power. Resolution does not rise linearly with power: test several powers and use the lowest one beyond which resolution stops improving. This also limits bleaching.

{{% /timelineItem %}}

{{% timelineItem icon="12" header=" " subheader="Save and transfer" badge="Save your data" %}}

- Select the sample name, open the three-dot menu and choose **Save as Copy**; choose a folder and **SAVE** (creates an `.obf` file).
- Open `.obf` files in Fiji by dragging them into the window (Bio-Formats).
- **New Sample** saves the current sample to your default folder and returns to dye selection.
- Copy your data off the computer over the network before you leave. See [Getting Started](/training/getting-started).

{{% /timelineItem %}}

{{% timelineItem icon="13" header=" " subheader="Shut down" badge="Finish Up" %}}

- close LiGHTBOX (select yes to turn off the microscope or no to leave the microscope running for the next user)
- remove your sample
- clean the oil off the objective with lens tissue
- switch off the controllers ( yellow labels <span style="color: black; background-color: yellow;">3</span>, <span style="color: black; background-color: yellow;">2</span>, <span style="color: black; background-color: yellow;">1</span>)
- leave the bench clean

{{% /timelineItem %}}

{{< /timeline >}}
