+++
title = 'Discovery.V20 Stereomicroscope'
layout = 'simple'
+++

## Overview

The [Zeiss Discovery.V20](https://www.zeiss.com/microscopy/en/products/light-microscopes/stereo-and-zoom-microscopes/stereo-discovery-v20.html) images meso- and macro-scale samples (whole organisms, embryos, dissected tissue, gels) in brightfield, darkfield, oblique and green/red fluorescence.

- Magnification with the 1x objective: 7.5x-150x through the eyepieces [camera/screen magnification differs].
- Camera: Zeiss AxioCam MRm, controlled by [Micro-Manager](https://micro-manager.org/) (runs inside ImageJ).
- The transmitted-light base has an adjustable mirror so you can change the illumination angle and enhance contrast. Good lighting is half the image.

{{< figure src="system.jpg" nozoom=true caption="System overview" >}}

## Safety and care

- The fluorescence lamp is a metal-halide source. Do not look directly into the light guide or turn it on without it connected. Let it warm up as per the lamp instructions; do not switch it off and on repeatedly.
- Keep fluids away from the optics and electronics. Use glass or black plates, never put dishes with liquid directly on the base.
- **Data transfer: see step 5. This computer is not on the network.**

## Imaging step by step

### 1. Choose your imaging mode

| Light from... | Modes |
|---|---|
| Below (transmitted) | Brightfield, darkfield, oblique |
| Above (reflected) | Brightfield, darkfield, oblique, fluorescence |

For transmitted light, set the [illumination sliders](sliders.png) using the guide below (click for the manual).

{{< figure src="transmittedLightSettings.png" href="SteREO Discovery Stereomicroscope - Operating Manual.pdf" nozoom=true caption="Transmitted light settings" >}}

### 2. Switch on

1. [Microscope](microscopeControl.png): press the button next to the power symbol on the control panel.
2. [Computer](computer.png): on the shelf next to the fluorescence lamp.
3. The light source you need:
   - [Transmitted LED](transmittedLight.png) (on the table behind the microscope): set the brightness.
   - [Reflected LED](reflectedLight.png) (above the transmitted LED): set the level I, II or III.
   - [Fluorescence lamp](excitation.png) (X-Cite 120, on the shelf): start with the attenuation dial **low** and increase only as needed, to limit bleaching.
4. Place the stage plate: the 120 mm **glass plate** for transmitted light, or the **black/white plate** for reflected light.

### 3. Set up the sample

1. Place the sample under the lens.
2. Adjust the light direction and intensity.
3. [Send the light to the eyepieces](lightpathEyes.png).
4. Set the zoom to the lowest value (7.5x).
5. [Focus](focusWheel.png), then zoom in and refocus.

### 4. Capture an image

1. [Send the light to the camera](lightpathCamera.png).
2. Log in as "Discovery User" [password: ask the facility].
3. Open the **Micro-Manager** shortcut on the desktop. (ImageJ opens first, which is normal.) Click **OK** to load the default configuration.
4. Under *Configuration settings > Magnification*, choose the setting that matches the microscope zoom so the image contains correct scaling metadata.
5. The camera image is flipped. Choose *Plugins > On-The-Fly Processors > Image Flipper*; the processor is already configured, so close the two windows that open.
6. Click **Live** to see the camera image. Adjust **exposure** and lighting using the histogram: no saturated pixels. Click **Stop** (or **Live** again) to stop.
7. Click **Snap**. The image opens in an ImageJ window where you can analyse or save it.
8. **Save to `D:/user data/<your name>/`.** Never save to the C: drive or desktop.

To collect several snaps, use **Album**; click **Save** to write the series to disk. [Micro-Manager user guide](https://micro-manager.org/Micro-Manager_User's_Guide).

### 5. Get your data off the computer

**Special case:** this computer runs an unsupported version of Windows and is **not connected to the network**.

1. Plug an approved USB drive into the front port.
2. Copy your files, then check they open on another computer.
3. Eject the drive safely.

### 6. Shut down

1. Close Micro-Manager.
2. Switch off the light sources and microscope.
3. Shut down the computer.
4. Return the stage plate and leave the area clean.

## Advanced: multi-dimensional acquisition

In Micro-Manager, **MultiD Acq.** collects [wavelength, time, z and XY](screenshots/multiDdimensions.png) series. This system supports **channels or time-lapse** only, not both at once.

### Fluorescence

The Pentafluar filter turret allows stereo viewing in fluorescence. Rotate the knurled wheel until the number on the front matches the label.

| Position | Filter |
|:-:|---|
| 1 | None (brightfield) |
| 2 | Green (GFP) [Zeiss set 38] |
| 3 | Red (Cy3/DsRed) [Zeiss set 43] |

{{< figure src="Cy3FilterControls.png" nozoom=true caption="Use the knurled dial at the red arrow to select the filter position." >}}

### Multichannel acquisition (manual filter change)

Filters are changed by hand. A Micro-Manager script prompts you at each channel.

1. First find the best exposure for each channel (set the filter, turn on the right light, check the histogram).
2. Choose *Tools > Script Panel* and run `ManualAcq2.bsh` (nothing visible happens yet).
3. Open **MultiD Acq.**, tick **Channels**, tick the channels in the "Use?" column, and enter each channel's exposure.
4. Click **Acquire!** and follow the pop-ups for each channel:
   - Brightfield: turret position 1, fluorescence off, transmitted or reflected light on.
   - GFP: turret position 2, white light off, fluorescence on.
   - Cy3: turret position 3.
   Click **OK** after each change.
5. Save your data as separate image files or one image stack ([details](https://micro-manager.org/Micro-Manager_User's_Guide)).

{{< gallery >}}
  {{< figure src="gallery/closed.jpg" caption="Closed" figureClass="grid-w33" >}}
  {{< figure src="gallery/open.jpg" caption="Open" figureClass="grid-w33" >}}
  {{< figure src="gallery/IR.jpg" caption="Open with IR filter (prevents heating up your sample)" figureClass="grid-w33" >}}
{{< /gallery >}}
