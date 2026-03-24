+++
date = '2026-03-18T12:18:49+01:00'
draft = false
title = 'Discovery.V20'
layout = 'simple'
showHero = true
heroStyle = 'background'
+++
## Overview
The [Discovery.V20 Stereomicroscope](https://www.zeiss.com/microscopy/en/products/light-microscopes/stereo-and-zoom-microscopes/stereo-discovery-v20.html) offers both transmitted and reflected brightfield microscopy as well as the ability to view green and red fluorophores of meso and macro sized samples. With our 1X lens, the system is capable of magnifications from 7.5X to 150X. Image acquisition is enabled through [micro-manager](https://micro-manager.org/) and a Zeiss [MRm camera](AxioCam-MRm3.pdf). Our transmitted light module contains continuously variable mirror adjustment mechanism with multiple degrees of freedom allowing you to adjust the illumination beams’ angle of incidence. In this way, you can establish the illumination needed to contrast different types of specimens. With Meso/Macro microscopy, the lighting and modality of imaging is an important component of the imaging workflow. 

## Imaging

{{< timeline >}}

{{< timelineItem icon="1" header=" " subheader="Decide on the Imaging Modality" badge="start here" md="true" >}}
{{< columns >}}
- **Transmitted Light Modes (Diascopic Illumination)**
	- Brightfield / Darkfield / Oblique Illumination	
- **Reflected Light Modes (Episcopic Illumination)**
	- Brightfield / Darkfield / Oblique Illumination
	- Fluorescence
{{< column >}}
If you're using transmitted light, set the [illumination sliders](sliders.png) according to the guide below. 
{{< figure
	src="transmittedLightSettings.png"
	href="SteREO Discovery Stereomicroscope - Operating Manual.pdf"
	nozoom=true
	caption="Transmitted Light Settings"
>}}
{{< endcolumns >}}

{{< /timelineItem >}}
{{< timelineItem icon="2" header=" " subheader="Turn On System" badge="Step 2" md="true" >}}
1. [Turn on the Microscope](microscopeControl.png). Button next to the &#x23FC; symbol on the microscope control panel.
1. [Turn on the Computer](computer.png). Computer sits on the shelf, next to the Excite EXFO-120 fluorescence light source.
1. Turn on the light source required for your imaging modality.
	- [Transmitted light source](transmittedLight.png). White light LED on the table behind the microscope. Also set the brightness of the light source. 
	- [Reflected light source](reflectedLight.png). White light LED on top of the transmitted light LED. Also set the level - I, II, or III.
	- [Epi-fluorecence light source](excitation.png). Excite EXFO-120 on the shelf. Also ensure that the attenuation dial is set to allow the maximum light into the light path. 
- For transmitted illumination, make sure to place &#8960;120mm glass plate in the stage to support your sample.
- Alternatively, if you're using reflected light, place the &#8960;120mm B/W plate in the stage to support your sample.
{{< /timelineItem>}}

{{< timelineItem icon="3" header=" " subheader="Place your Sample and configure the system" badge="Initial Image" md="true" >}}
1. Put your sample under the microscope lens.
1. Adjust the lighting appropriately.
1. [Set the light path to send the light to your eyes](lightpathEyes.png).
1. Set the zoom to the lowest magnification (7.5X)
1. [Focus](focusWheel.png)
1. Adjust zoom and focus to create the image you require.
{{< /timelineItem>}}

{{< timelineItem icon="4" header=" " subheader="Capture an Image" badge="Image Acquisition" md="true" >}}
1. [Change the light path to send light to the camera](lightpathCamera.png). 
1. Login to the computer as the "Discovery User".
1. Start the acquisition software - Double-click on the [Micro-Manager shortcut](screenshots/mmIcon.png) on the desktop. Starting Micro-Manager will also start ImageJ (in fact, ImageJ starts up first and runs Micro-Manager as a plugin).
1. Click "OK" on the [splash screen](screenshots/splash.png) to load the default hardware configuration. The Micro-Manager [user interface](screenshots/mm.png) will launch.
1. Click on "7.5X" in the [Magnification row in the "configuration settings"](settings/magnifications.png) box. This will let you set the magnification to match the microscope's magnification, ensuring the correct scaling of your image. NB only magnifications that are multiples of 10 contain scaling information.
1. By default, the camera orientation reasults in a flipped image when compared to the sample. To flip the image to match the sample, click on [*Plugins->On-The-Fly Processors->Image Flipper*](screenshots/flipper.png). This will open the [Image Flipper](screenshots/reverse.png) configurator panel. The Image Flipper is already configured correctly, you can close the two windows that open by X-ing out of them, activating the image flipper. Your image should now be [correctly oriented](screenshots/corrected.png).  
1. Click on the "Live" Button in the [acquisition](screenshots/acqusition.png) pane to see a continuously updated, “live” view from the camera. The images will be displayed in the [“Live” window](screenshots/imageWindow.PNG). Pressing this button again, stops live mode.
1. Use the live image and image histogram to adjust the [exposure time](screenshots/exposure.png) & lighting intensity to your requirements.
1. Click on the "Stop" button in the acquisition software to stop the "Live" imaging window. 
1. Click on the "Snap" button (main window or image window) in the acquisition software to snap an image using the parameters in the main MM window. This acquires a single image from the camera. A display window will pop up with the acquired still image. You can use any of the available ImageJ tools to analyze, save or edit the image. In addition, at the bottom of the window there are shortcut buttons to save the image, enter live mode or send images to album.
1. Save the image to your Data folder. Create a folder on the D:/user data/ folder to store your data. Do not store images on the C:/ drive - this includes the desktop.

With the “Album” button, you can collect a series of still images (snaps) in an image series window. The first time you click the “Album” button, a new series window will open, with a fresh image obtained from the camera. Every time you click the “Album” button thereafter, a new image will be added to the series. Click the “Save” button to write all images in the series window to disk.

[More information about Micro-Manager operation and Documentation](https://micro-manager.org/Micro-Manager_User's_Guide).

{{< /timelineItem>}}

{{< timelineItem icon="5" header=" " subheader="Retrieve Your Image Data" badge="Copy Data to Device" md="true" >}}
Because this version of windows is no longer supported by microsoft, this computer is no longer allowed to connect to the network. Therefore all data must be copied from the computer's hard drive to a USB/Firewire device.


1. Plugin a USB device to the front USB port of the computer. 
1. Copy your image data to your device.
1. Eject your device.
{{< /timelineItem>}}
{{< timelineItem icon="6" header=" " subheader="When you are finished" badge="Turn off the system" md="true" >}}
1. Turn off the microscope
1. Turn off the light source
1. Shut down the computer
{{< /timelineItem>}}


{{< /timeline >}}

## Advanced Acquisition
### Multi-Dimensional Acquisition
Micro-Manager enables the ability to capture multiple images from different dimensions ([wavelength, time, z, xy](screenshots/multiDdimensions.png)) and treat them as a single image or image series. Our stereomicroscope can only take advantage of [two of these extra dimensions](screenshots/multiDtimeChannel.png). You can either activate multiple channel acquisition or timelapse acquisition in the Multi-Dimensional Acquisition window that opens by pressing the ["MultiD Acq. button"](screenshots/MultiDbutton.png) in the MM main windown.

### Fluorescence imaging
Our Discovery V.20 has a pentafluor fluorescence filter turret that places filter cubes into the light path for both eyes, allowing stereo fluorescence viewing. We have filter cubes for [green](https://www.micro-shop.zeiss.com/en/uk/fluorescenceAssistant/filtersets/000000-1031-346) and [red](https://www.micro-shop.zeiss.com/en/uk/fluorescenceAssistant/filtersets/488043-9100-400) dyes.

1. 