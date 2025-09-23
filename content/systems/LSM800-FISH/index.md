+++
date = '2025-08-29T09:38:42+01:00'
draft = false
title = 'LSM800 FISH'
showHero = true
layout = 'simple'
heroStyle = 'background'
+++
## Overview
Designed for imaging fixed samples in fluorescence mode, this LSM800 is equipped with 4 lasers, 3 detectors (one Airyscan), and a variety of lenses for imaging samples with varying length scales, from cells to fish. Samples for this system should be mounted on slides under coverslips, or in petri dishes. This system is configured to accommodate blue, green, red and far red fluorophores either individually, or in combination. Acquisition software is Zeiss' Zen version 2.6. The software enables collection of X/Y planes from 128 X 128 pixels up to 4096 X 4096 pixels, Z-stacks, time-lapse, and tiles. The Airyscan detector **can** improve the resolution of your image up to 2X. 

{{< columns >}}
- Lasers: <span style="background-color:purple">&nbsp;405nm&nbsp;</span>, <span style="background-color:cyan;">&nbsp;488nm&nbsp;</span>, <span style="background-color:orangered;">&nbsp;561nm&nbsp;</span>, <span style="background-color:darkred;">&nbsp;642nm&nbsp;</span>
- Lenses: 20X/0.8, 20X/1.0 Water Imm, 40X/1.3 Oil, 63X/1.4 Oil
- Stand: Axio Examiner.Z1 Fixed Stage
- Detectors: 2X GAsP, 1X Airyscan
- Typical Fluorophores: DAPI, Alexa488, EGFP, Rhodamine, mCherry, Alexa546, Alexa568, Alexa647, Cy5
- LSM800 scanner with two variable spectral dichroic mirrors to direct distinct wavelength the emission fluorescence into three separate
{{< column >}}{{< figure src=LSM800.png
	default=true >}}
{{< endcolumns >}}
{{< figure src=LSM800LightPath.png 
	default=true
	caption="LSM 800 Light path"
	class="center" >}}
The two VSDs act in concert to separate the emission light and send the appropriate wavelengths to the correct detector. The 1st VSD is a longpass filter, sending the shorter wavelengths to GAsP detector 1 and the longer wavelengths to detectors 2 and 3. The 2nd VSD is a shortpass filter, sending shorter wavelengths to the Airyscan detector and longer wavelengths to GSsdP detector 3. Further refinement of the exact wavelengths reaching each detector can be achieved with filters from the emission filter wheels placed in front of each of the two GAsP detectors.

## Getting Started
### How to collect your first image. SOP
#### <span style="background-color:slategray;">&nbsp;Turning on the system&nbsp;</span>
{{< columns >}}
<ol start="0">
<li>If the system is switched off at the wall, switch on the system at the wall &mdash; 2 @ the red UPS connected sockets and 1 for the HXP lamp above the electronics tower. &mdash; <span style="background-color:orange;color:black;border-radius:50px;">&nbsp;0&nbsp;</span></li>
<li>Switch on System/PC &mdash; <span style="background-color:orange;color:black;border-radius:50px;">&nbsp;1&nbsp;</span></li>
<li>Switch on Components &mdash; <span style="background-color:orange;color:black;border-radius:50px;">&nbsp;2&nbsp;</span></li>
<li>Switch on Laser Key &mdash; turn key from vertical to horizontal --- <span style="background-color:orange;color:black;border-radius:50px;">&nbsp;3&nbsp;</span></li>
<li>Switch on the HXP lamp &mdash; <span style="background-color:orange;color:black;border-radius:50px;">&nbsp;3.5&nbsp;</span></li>
<li>Switch on the computer &mdash; <span style="background-color:orange;color:black;border-radius:50px;">&nbsp;4&nbsp;</span></li>
<li>Open ZEN software using desktop icon, wait for the splashscreen to appear, and select "ZEN system" to connect to the microscope. &mdash; <span style="background-color:orange;color:black;border-radius:50px;">&nbsp;5&nbsp;</span></li>
</ol>
{{< figure src=computer.png 
	default=true
	class="center" >}}
{{< column >}}
{{< figure src=ElectronicsTower.png 
	default=true
	caption="Lasers/System Startup Cabinet"
	class="center" >}}
{{< endcolumns >}}

#### <span style="background-color:slategray;">&nbsp;Zen Overview&nbsp;</span>
As detailed in the figure below, the acquisition controls placed in the left third of the screen, the image windows are in the middle half of the screen, with image display controls situated underneath the image. Finally, the image saving and project controls are on the far right of the screen.
{{< figure src=ZenOverview.png 
	default=true
	caption="Zen Workspace default UI"
	class="center" >}}
#### <span style="background-color:slategray;">&nbsp;Place your sample on the Microscope&nbsp;</span>
This confocal microscope uses an AxioImager.Z1 stand. It has a fixed position stage, focusing moves the lens up or down. It has a manually rotating objective lens turret. To accommodate samples of different sizes the entire lens moves from a "load" position, far away from your sample, to an "imaging" position, with the front lens near your sample. Moving from one lens to the other is achieved by rotating the big black knob on the front of the microscope, near the lens turret.
{{< columns >}}
{{< figure src=AxioImagerUp.jpg 
	default=true
	width=200px
	caption="Lens in the 'load' position"
	class="center" >}}
{{< column >}}
{{< figure src=AxioImagerDown.jpg 
	default=true
	width=200px
	caption="Lens in the imaging position"
	class="center" >}}
{{< endcolumns >}}
#### <span style="background-color:slategray;">&nbsp;Locate Your Sample&nbsp;</span>
The next part of the procedure, focusing your sample, is the trickiest bit at first. Without experience, this is the step where you will struggle initially. With upright microscopes, it is very easy to lower the lens enough while focusing that you focus through your sample, without seeing it, breaking the slide. Perseverance and practice are the keys to feeling the ZEN of microscopy --- not to be confused with Zeiss' ZEN software.
While you are viewing the sample through the eyepieces, it can be helpful to have the "locate" tab selected in the software to see the status of the microscope hardware and to open/close shutters, *et cetera*.
{{< figure src=locate.png 
	default=true
	caption="Locate tab selected in the acquisition software"
	>}}

1. Place your sample on the stage, coverslip facing up.
1. Select the a lens and rotate it into position using the silver wheel found at the top of the lens turret. 
1. Depending on the lens you are using, make sure you have used the appropriate immersion media placed on top of your sample.
1. Lower the lens into the imaging position using the black rotating knob. --- <span style="background-color:orange;color:black;border-radius:50px;">&nbsp;6&nbsp;</span>
1. If using immersion media, focus the lens until it makes contact with the media.
1. Using the "Locate" tab in the software, activate the contrast method you will use to focus. This is usually a transmitted light mode or DAPI fluorescence. Press the button to turn on the light.
1. Check that the light path will send the light to the eyepieces and not the confocal scanhead.
1. ***Carefully***, while looking through the lens, continue to ***slowly*** lower the lens to focus your sample.
1. Use the joystick on the stage controller to find an appropriate field of view.
1. You are done with the microscope. Move the reflector turret to an open position (position 4 or 5), and change the ligthpath selector to direct the transmitted light or the emitted fluorescence light to the scanhead.






