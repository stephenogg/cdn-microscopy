+++
date = '2025-08-29T09:39:26+01:00'
draft = false
title = 'LSM880 - Inverted'
+++
## Overview

A Zeiss LSM880 laser-scanning confocal on an **inverted** stand (objectives below the sample), for **live-cell and fixed samples** in dishes, chambers, well plates and slides. [Airyscan: confirm whether this system has an Airyscan detector, and add the mode here if so.]

| Item | Specification |
|---|---|
| Stand | Inverted: the objective sits below the sample and the stage holds it from above |
| Lasers | 405, 458, 488, 514, 561, 633 nm |
| Objectives | 10x/0.3; 20x/0.8; 40x/1.1 Water; 40x/1.3 Oil; 63x/1.4 Oil |
| Eyepiece filter cubes | Fs38 (green), Fs43 (red), Fs49 (blue/UV) |
| Environment | Temperature control and CO<sub>2</sub> for Ibidi chambers, 35 mm dishes and 24-well plates |
| Software | ZEN 2.3 SP1 (**black edition**). |

> [!NOTE] ZEN black, not ZEN blue
> This system runs **ZEN black**. The layout differs from ZEN blue on the LSM800 and other systems. Instructions written for ZEN blue will not match what you see.

Eyepiece filter cubes (used for finding the sample by eye):

| Colour | Filter | Excitation | Dichroic | Emission |
|---|---|---|---|---|
| Green | Fs38 | 470/40 | FT495 | 525/50 |
| Red | Fs43 | 545/25 | FT570 | 605/70 |
| Blue | Fs49 | G365 | FT395 | 445/50 |

## Safety

- Lasers: 405, 458, 488, 514, 561, 633 nm. Never remove covers, and never look into the beam or at the objective with a laser on.
- Live samples: follow your approved biosafety level. Wipe up spills at once and report them.
- Immersion oil and water: use only the medium the objective is designed for. Never put oil on a water lens. Wipe spills at once.
- **Inverted stage:** spilled medium and oil can run into the objective and turret. Do not overfill dishes or wells, and check the outside of the vessel is dry.
- Do not touch the objective or force the stage. Report broken dishes, slides or spills immediately.

## 1. Switch on


1. Switch on the *main power (1)* *systems/PC (2)* and *Components (3)* switches.
1. Turn on the computer (4) and log in. Use the **LSM User** account - no Password.
1. Start **ZEN black** from the desktop icon. On the start-up screen choose **Start System** (not *Image Processing*, which allows no microscope control).
1. If you need temperature or CO<sub>2</sub> control, switch on the incubation unit **at least [30-60] minutes before imaging**, so the stage and sample are stable.

## 2. Know the ZEN black layout

- **Top-Left** the main workflow tabs: **Locate**, **Acquisition**, **Processing**, **Maintain**.
- Use the **Locate** tab to find/focus your sample, and check fluorescence levels.
- Use the **Acquisition** tab to acquire image data. This tab has many collapsible panels for **Light Path**, **Channels**, **Acquisition Mode**, **Z-Stack**, **Time Series**, **Tiles** and others. Tick **Show All** to see every panel.
- **Centre:** image display, with display controls below it.
- **Right:** the images and Documents gallery and image properties.
- **Just below the workflow tabs** are buttons that control the scanner.  the **Live**, **Snap**, and **Continuous** buttons, and **Start Experiment** for multi-dimensional runs.

## 3. Load your sample

1. Check the objective for the medium you need and that it is clean.
2. Lower the objective with the focus control (or click on the **Load Position** button on the stand display) before loading, so nothing can strike the sample.
3. Place the dish, plate or slide on the stage with the sample **facing down toward the objective**. Slides go **coverslip down**.
4. Secure it in the correct stage insert for your sample holder.
5. If you use immersion, add one small drop of the **correct** medium to the objective first, then, *while viewing the stage/sample*, raise the objective slowly until it contacts the sample.

## 4. Find your sample

1. In the **Locate** tab, choose the eyepiece mode (for example **DAPI**, **GFP**, **RFP**, **BF**) to set the matching filter cube and switch the emission to teh eyepieces.
2. Select the objective in the **Objectives** panel (or **Locate**). Choose a low-power lens first.
3. Looking through the eyepieces, focus **slowly**.
4. Use the stage controls or joystick to find a field of view.
5. Once you find your field of view and focus, click on the **OFF** button to prevent photobleaching of your sample.

## 5. Set up the acquisition

1. Go to the **Acquisition** tab. Click on the **Smart Setup** button to open the smart setup pane. Click **+** to add each dye in your sample, or load a saved setup with **Load** in **Light Path**.
2. Choose how to acquire the channels:
   - **Best Signal**: one channel at a time, least cross-talk, slowest. **Highly-Recommended for fixed multicolour samples.**
   - **Fastest**: channels together, quickest, most cross-talk.
   - **Smartest (line)**: switches line by line; a compromise.
3. In **Channels**, check each track: laser, **laser power**, **detector gain** and the detection **emission range**.
4. Keep the pinhole at **1 Airy unit** unless you have a reason to change it. Set it on one channel; ZEN black links the others.

## 6. Scan

Three buttons start and stop scanning (click again to stop):

| Button | What it does |
|---|---|
| **Live** | Fast scan of the current track only, for finding and focusing. Alwasy 512 X 521 and fastest scanning speed |
| **Continuous** | Scans with your **Acquisition Mode** settings, for previewing speed and quality. |
| **Snap** | One image of all ticked tracks, with the **Acquisition Mode** settings. |

Before the final image, switch on the **Range Indicator** in the display controls so saturated pixels show in colour, then lower laser power or gain until they disappear.

## 7. Optimise each channel

- **Pixel size**: in **Acquisition Mode**, set the frame size, then click **Optimal** (Nyquist) and use the **same** frame size for all channels.
- **Intensity**: keep laser power low, especially for live cells. Raise gain before laser power; avoid saturation.
- **Noise**: use averaging (for example 2-4 lines or frames) or a slower scan speed.
- **Bit depth**: use **16 bit** for quantitative work.
- **Pinhole**: 1 Airy unit.

## 8. Live-cell imaging

- Allow the stage and chamber to reach temperature before imaging, to prevent **focus drift**.
- Use the **lowest laser power** and fewest frames that answer your question; light kills cells.
- Use **Time Series** for time-lapse, **Z-Stack** for volumes, and **Tiles** for large areas. Open each panel and tick it for the **Start Experiment** button.
- Keep Z-stack ranges short. Check for **focus drift** in long runs. [Add Definite Focus status for this system if present.]
- Use **water or oil only as the lens requires**. For the 40x/1.1 Water lens, check the water supply and top up carefully during long runs.

## 9. Save and shut down

1. **Save** your images in ZEN's **.czi** format in your own folder, then close ZEN.
2. Copy your data to RDS ([how?](/protocols/map-network-drive)), check it, then delete it from the computer.
3. Remove your sample, and **clean the objective** with lens tissue (oil objectives: lens tissue, then cleaning fluid if needed). Wipe up any spills on the stage.
4. Clear the stage inserts and switch off the incubation unit.
5. If another user starts within [30] minutes, leave the hardware on and stop here.
6. Otherwise: close ZEN; set the **Argon laser to Standby** and wait for the fans to cool [about 5 minutes] before switching off the system; switch off the computer (4), switch off **Components (3)**, then **System/PC (2)** and finally **Main Power (1)**.
