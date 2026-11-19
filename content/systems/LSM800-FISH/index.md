+++
title = 'LSM800 (FISH)'
layout = 'simple'
+++

## Overview

A Zeiss LSM800 laser-scanning confocal with Airyscan, for **fixed samples in fluorescence**, from single cells to whole zebrafish. Samples go on slides under coverslips, or in dishes.

| Item | Specification |
|---|---|
| Stand | Axio Examiner.Z1: fixed stage, the objective moves to focus (**upright**) |
| Lasers | 405, 488, 561, 642 nm |
| Objectives | 20x/0.8; 20x/1.0 Water (dipping); 40x/1.3 Oil; 63x/1.4 Oil |
| Detectors | 2 x GaAsP, 1 x Airyscan |
| Typical dyes | DAPI, Alexa 488, EGFP, rhodamine, mCherry, Alexa 546/568/647, Cy5 |
| Image size | 128 x 128 to 4096 x 4096 pixels; Z-stacks, time series, tiles |
| Software | ZEN 2.6 (blue edition) |

Objective turret and fluorescence filter turret are **manual** on this system. Eyepiece filter cubes:

| Position | Colour | Filter | Excitation | Dichroic | Emission |
|:-:|---|---|---|---|---|
| 1 | Green | Fs38 | 470/40 | FT495 | 525/50 |
| 2 | Red | Fs43 | 545/25 | FT570 | 605/70 |
| 3 | Blue | Fs49 | G365 | FT395 | 445/50 |

{{< figure src="LSM800.png" default=true >}}

> [!WARNING] Dipping objective
> The 20x/1.0 Water lens is a dipping objective for use in water or buffer only. Never use oil with it; rinse and dry it afterwards.


## Light path and detectors

The scanner has **two GaAsP detectors and one Airyscan detector**. Two variable secondary dichroics (VSDs) split the emission: the 1st sends shorter wavelengths to GaAsP detector 1 and longer ones onward; the 2nd sends shorter wavelengths to the Airyscan and longer ones to GaAsP detector 3.  Emission filter wheels in front of the GaAsP detectors narrow the range further.

{{< figure src="LSM800LightPath.png" default=true caption="LSM800 light path" class="center" >}}

| GaAsP detector 1 filters | GaAsP detector [2/3] filters |
|---|---|
| SP470, SP545, SP620 | LBF640, LP575, LP655, SP620 |

{{< figure src="VSDAnimation.gif" default=true caption="" class="center" >}}

**Airyscan** improves resolution up to about 1.7x (roughly 120 nm lateral at best) compared with standard confocal. It works best on thin, bright, well-labelled samples; needs Airyscan sampling and processing; and is slower. Use standard confocal if you only need counting or colocalisation at normal resolution.

## Safety

- Lasers: 405, 488, 561, 642 nm. Never remove covers, and never look into the beam or at the lens with the laser on.
- Do not switch the HXP lamp on and off repeatedly; it has 20 minute warm-up and cool-down.
- Immersion oil and water: wipe spills at once; never use oil with a water or dry lens.
- Report broken slides or spills immediately; do not clean glass on the stage with your fingers.

## 1. Switch on

1. If the wall sockets are off, switch them on: two red (UPS) sockets and one for the HXP lamp (above the electronics tower).
2. In the electronics cabinet, switch on **System/PC**, then **Components** on the PSU module.
3. Turn the **laser key** from vertical to horizontal. Wait for the white LED to go out and a faint beep before continuing.
4. Switch on the **HXP lamp**.
5. Switch on the computer and wait for Windows to log in.
6. Open ZEN. Nothing appears for a while, so be patient. Choose **ZEN system** on the splash screen and wait for the interface.

{{< figure src="ElectronicsTower.png" default=true caption="Laser/system start-up cabinet" class="center" >}}
{{< figure src="computer.png" default=true class="center" >}}

## 2. Know the ZEN layout

Acquisition controls are on the left, images in the middle (display controls beneath), and saving and project controls on the right.

{{< figure src="ZenOverview.png" default=true caption="ZEN workspace" class="center" >}}

## 3. Load your sample

The objective moves between a **load** position (far from the sample) and an **imaging** position using the large black knob near the turret.

{{< columns >}}
{{< figure src="AxioImagerUp.jpg" default=true width=200px caption="Lens in load position" class="center" >}}
{{< column >}}
{{< figure src="AxioImagerDown.jpg" default=true width=200px caption="Lens in imaging position" class="center" >}}
{{< endcolumns >}}

## 4. Find your sample (the tricky part)

{{< alert icon="circle-exclamation" cardColor="#e63946" >}}
**On an upright microscope it is easy to focus through the slide and break it. Always move the lens slowly, looking from the side.**
{{< /alert >}}

1. Place the sample with the **coverslip facing up**.
2. Select the objective with the turret wheel.
3. Add immersion medium if the objective needs it (oil for the 40x/1.3 and 63x/1.4; water only for a water objective).
4. Lower the lens **slowly** with the black knob. The lens may drop onto the sample, depending on the last user's settings.
5. If using immersion, focus until the lens touches the medium.
6. In the **Locate** tab choose a mode (BF, DAPI, GFP, RFP) and turn the light on. Select the matching filter cube (manual turret).
7. Looking through the eyepieces, **slowly** focus.
8. Use the stage joystick to find a field of view.
9. **Before scanning**, set the reflector turret to an open position (4 or 5) and set the light path so light goes to the scan head.

{{< figure src="locateTab.png" default=true width=400px class="center" >}}

## 5. Configure the acquisition

1. Go to the **Acquisition** tab and click **Smart Setup**.
2. Click **+** to add a dye, and select every dye in your sample.
3. Choose the mode: **LSM** (confocal) or **Airyscan SR**.
4. Choose how to acquire the channels:
   - **Best Signal**: one channel at a time, least cross-talk, slowest. **Recommended for fixed multicolour samples.**
   - **Fastest**: channels together, quickest, most cross-talk.
   - **Smartest (line)**: switches channel line by line; a compromise.

{{< figure src="drawing.svg" default=true caption="Acquisition tab" class="center" >}}
{{< figure src="smartSetup.svg" default=true caption="Smart Setup pane" class="center" >}}

## 6. Scan

Three buttons start and stop scanning (click again to stop):

| Button | What it does |
|---|---|
| **Live** | Fastest scan: 512 x 512, no averaging, current track only. |
| **Continuous** | Scans with your Acquisition Mode settings, to preview speed and quality. |
| **Snap** | One image of all ticked tracks, with the Acquisition Mode settings. |

{{< figure src="acquisitionTab.svg" default=true class="center" >}}

## 7. Optimise each channel

Set these before your final image:

- **Pixel size** (resolution)
- **Intensity range** (laser power, gain): no saturated pixels (use the Range Indicator)
- **Noise** (averaging, scan speed)
- **Pinhole**: 1 Airy unit unless you have a reason to change it

**Pixel size:** click **Optimal** to set Nyquist sampling for standard confocal. Set it on one channel and keep it for all channels, so they overlay. For Airyscan SR, use the Airyscan sampling that ZEN sets; do not use the confocal Optimal value.

**How a confocal builds an image:** a focused laser spot is scanned across the sample in rows (a raster), and a point detector converts the emitted photons at each position into one pixel.

{{< figure src="raster.svg" caption="Raster scan pattern used to build a 2D image." >}}

## 8. Save and shut down

1. Save your images and close ZEN.
2. Copy your data to RDS ([how](/protocols/map-network-drive)), check it, then delete it from the computer.
3. Remove your sample, and clean immersion media from the lens with lens tissue.
4. If another user starts within 30 minutes, leave the hardware on and stop here.
5. Otherwise: shut down Windows; switch off the HXP lamp; turn the laser key; switch off **Components** then **System/PC**; switch off the three wall sockets.
