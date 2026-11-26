+++
date = '2025-08-29T09:39:17+01:00'
draft = false
title = 'LSM880-Upright'
+++
## Overview

A Zeiss LSM880 laser-scanning confocal on an **upright** stand (objectives above the sample), for **fixed samples on slides and live or fixed samples in dishes, using dipping lenses**. 

| Item | Specification |
|---|---|
| Stand | Upright: the objective is above the sample, Axio Examiner |
| Lasers | 405, 440, 458, 488, 514, 561, 594, 633 nm |
| Objectives | 5x/0.16; 10x/0.45 Water (dipping); 20x/0.8; 20x/1.0 Water (dipping); 40x/1.0 Water (dipping); 63x/1.4 Oil |
| Eyepiece filter cubes | Fs38 (green), Fs43 (red), Fs49 (blue/UV) |
| Software | ZEN 2.3 SP1 (**black edition**).|

> [!NOTE] ZEN black, not ZEN blue
> This system runs **ZEN black**. The layout differs from ZEN blue on the LSM800 and other systems. Instructions written for ZEN blue will not match what you see.

Eyepiece filter cubes (used for finding the sample by eye):

| Colour | Filter | Excitation | Dichroic | Emission |
|---|---|---|---|---|
| Green | Fs38 | 470/40 | FT495 | 525/50 |
| Red | Fs43 | 545/25 | FT570 | 605/70 |
| Blue | Fs49 | G365 | FT395 | 445/50 |

> [!WARNING] Dipping objectives
> The 10X/0.45, 20x/1.0 and 40x/1.0 Water lenses dip directly into water or buffer. **Never use oil with them.** Rinse with water and dry them with lens tissue afterwards.

## Safety

- Lasers: 405, 440, 458, 488, 514, 561, 594, 633 nm. Never remove covers, and never look into the beam or at the objective with a laser on.
- Live or fixed biological samples: follow your approved biosafety level.
- Immersion oil and water: use only the medium the objective is designed for. Never use oil on a water lens. Wipe spills at once.
- **Upright stand:** it is easy to drive the lens into the slide or dish and break it. Always lower the lens slowly, looking from the side.
- Report broken slides, dishes or spills immediately. Do not clean glass on the stage with your fingers.

## 1. Switch on

1. Switch on the **main power**, **System/PC** and **Components** switches.
2. Switch on the fluorescence lamp if you need it.
3. Turn on the computer and log in. No password required.
4. Start **ZEN black** from the desktop icon. On the start-up screen choose **Start System** (not *Image Processing*, which has no microscope control).


## 2. Know the ZEN black layout

- **Top-Left** the main workflow tabs: **Locate**, **Acquisition**, **Processing**, **Maintain**.
- Use the **Locate** tab to find/focus your sample, and check fluorescence levels.
- Use the **Acquisition** tab to acquire image data. This tab has many collapsible panels for **Light Path**, **Channels**, **Acquisition Mode**, **Z-Stack**, **Time Series**, **Tiles** and others. Tick **Show All** to see every panel.
- **Centre:** image display, with display controls below it.
- **Right:** the images and Documents gallery and image properties.
- **Just below the workflow tabs** are buttons that control the scanner.  the **Live**, **Snap**, and **Continuous** buttons, and **Start Experiment** for multi-dimensional runs.h

## 3. Load your sample

1. Raise the objective to the **load** position, well clear of the stage. You can press the "Load" button or use the focus wheel.
2. Place the slide with the **coverslip facing up**, or the dish on the stage, and secure it.
3. Select the objective in the **Objectives** panel (or **Locate**). Start with a low-power lens.
4. Add immersion medium if the objective needs it: oil for the 63x/1.4; **water only** for the water lenses. For dipping lenses, make sure the sample is covered in water or buffer.

## 4. Find your sample (the tricky part)

{{< alert icon="circle-exclamation" cardColor="#e63946" >}}
**On an upright microscope it is easy to focus through the slide and break it. Always move the lens slowly, looking from the side.**
{{< /alert >}}

1. Lower the lens **slowly** until it nearly touches the slide or the medium. Look from the side, not at the screen.
2. In the **Locate** tab, choose the eyepiece mode (for example **DAPI**, **GFP**, **RFP**, **BF**) to set the matching filter cube and switch on the lamp.
3. Looking through the eyepieces, focus **slowly upward** (away from the sample), never downward.
4. Use the stage controls to find a field of view.


## 5. Set up the acquisition

1. Go to the **Acquisition** tab. Open **Smart Setup** and click **+** to add each dye in your sample, or load a saved setup with **Load** in **Light Path**.
2. Choose how to acquire the channels:
   - **Best Signal**: one channel at a time, least cross-talk, slowest. **Recommended for fixed multicolour samples.**
   - **Fastest**: channels together, quickest, most cross-talk.
   - **Smartest (line)**: switches line by line; a compromise.
3. In **Channels**, check each track: laser, **laser power**, **detector gain** and the detection **emission range**.
4. Keep the pinhole at **1 Airy unit** unless you have a reason to change it.

## 6. Scan

Three buttons start and stop scanning (click again to stop):

| Button | What it does |
|---|---|
| **Live** | Fast scan of the current track only, for finding and focusing. |
| **Continuous** | Scans with your **Acquisition Mode** settings, for previewing speed and quality. |
| **Snap** | One image of all ticked tracks, with the **Acquisition Mode** settings. |

Before the final image, switch on the **Range Indicator** in the display controls so saturated pixels show in colour, then lower laser power or gain until they disappear.

## 7. Optimise each channel

- **Pixel size**: in **Acquisition Mode**, set the frame size and zoom, then click **Optimal** (Nyquist) and use the **same** frame size for all channels.
- **Intensity**: keep laser power low. Raise gain before laser power; avoid saturation.
- **Noise**: Reduce noise by averaging (for example 2-4 lines or frames) or a slower scan speed.
- **Bit depth**: use **16 bit** for quantitative work.
- **Pinhole**: 1 Airy unit.
- **Z-Stack**, **Time Series** and **Tiles**: open each panel and tick it for **Start Experiment**. Use the **Z-Stack** panel's **Optimal** interval for 3D.
- **Depth:** dipping water lenses reach deeper into cleared or thick tissue, but signal drops with depth. Increase laser power or gain with depth only in the **Z-Stack** panel's **Z-Brightness correction**. [Confirm.]

## 8. Save and shut down

1. **Save** your images in ZEN's **.czi** format in your own folder, then close ZEN.
2. Copy your data to RDS ([how?](/protocols/map-network-drive)), check it, then delete it from the computer.
3. Raise the objective, remove your sample, and **clean immersion media** from the lens with lens tissue. Rinse and dry dipping lenses after use.
4. If another user starts within [30] minutes, leave the hardware on and stop here.
5. Otherwise: close ZEN; set the **Argon laser to Standby** and wait for it to cool [about 5 minutes]; switch off the computer. Switch off the lamp, **Components**, then **System/PC** and finally the **Main Power**.