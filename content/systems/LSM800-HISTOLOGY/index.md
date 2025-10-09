+++
date = '2025-08-29T09:38:51+01:00'
draft = false
title = 'LSM800 HISTOLOGY'
showHero = true
heroStyle = 'background'
+++

<details>
  <summary>{{< icon "chevron-down" >}} Overview</summary>

## Overview
Designed for imaging fixed samples in fluorescence mode, this LSM800 is equipped with 4 lasers, 3 detectors (one Airyscan), and a variety of lenses for imaging samples with varying length scales, from cells to fish. Samples for this system should be mounted on slides under coverslips, or in petri dishes. This system is configured to accommodate blue, green, red and far red fluorophores either individually, or in combination. Acquisition software is Zeiss' Zen version 2.6. The software enables collection of X/Y planes from 128 X 128 pixels up to 4096 X 4096 pixels, Z-stacks, time-lapse, and tiles. The Airyscan detector **can** improve the resolution of your image up to 1.7X. 

{{< columns >}}
- Lasers: <span style="background-color:purple">&nbsp;405nm&nbsp;</span>, <span style="background-color:cyan;">&nbsp;488nm&nbsp;</span>, <span style="background-color:greenyellow;">&nbsp;561nm&nbsp;</span>, <span style="background-color:darkred;">&nbsp;642nm&nbsp;</span>
- Lenses: 10x/0.45, 20X/0.8, 40X/1.3 Oil, 63X/1.4 Oil
- Stand: Axio Imager.Z1
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
The two VSDs (Variable Secondary Dichroics) act in concert to separate the emission light and send the different wavelengths to the correct detector. Briefly, the 1<sup>st</sup> VSD acts as a longpass filter, sending the shorter wavelengths to GAsP detector 1 and the longer wavelengths to detectors 2 and 3. The 2<sup>nd</sup> VSD is a shortpass filter, sending shorter wavelengths to the Airyscan detector 2 and longer wavelengths to GAsP detector 3. Further refinement of the exact wavelengths reaching each detector can be achieved with filters from the emission filter wheels placed in front of each of the two GAsP detectors.


{{< columns >}}
Detector 1 filters:
- SP470
- SP545
- SP620
{{< column >}}
Detector 2 filters:
- LBF640
- LP575
- LP655
- SP620
{{< endcolumns >}}


{{< figure src=VSDAnimation.gif
	default=true
	caption=""
	class="center" >}}
</details>
<details>
  <summary>{{< icon "chevron-down" >}} Turn ON the system</summary>

#### <span style="background-color:slategray;">&nbsp;Turning on the system&nbsp;</span>
{{< columns >}}
<ol start="0">
<li>If the system is switched off at the wall, switch on the system at the wall &mdash; 2 @ the red UPS connected sockets and 1 for the HXP lamp above the electronics tower. &mdash; <span style="background-color:orange;color:ghostwhite;border-radius:50px;">&nbsp;0&nbsp;</span></li>
<li>Switch on System/PC switch on the PSU module &mdash; <span style="background-color:orange;color:ghostwhite;border-radius:50px;">&nbsp;1&nbsp;</span></li>
<li>Switch the Components switch on on the PSU module &mdash; <span style="background-color:orange;color:ghostwhite;border-radius:50px;">&nbsp;2&nbsp;</span></li>
<li>Turn the Laser Key &mdash; from vertical to horizontal &mdash; <span style="background-color:orange;color:ghostwhite;border-radius:50px;">&nbsp;3&nbsp;</span></li>
<ul>
	<li>Wait for the white LED on the laser module to go off and listen for a faint audible signal indicating lasers are initialised, before proceeding.</li>
</ul>
<li>Switch on the HXP lamp &mdash; <span style="background-color:orange;color:ghostwhite;border-radius:50px;">&nbsp;3.5&nbsp;</span></li>
<li>Switch on the computer &mdash; <span style="background-color:orange;color:ghostwhite;border-radius:50px;">&nbsp;4&nbsp;</span></li>
<li>Waaaaaiiiiiiiit until Windows boots and automatically logs in. Open ZEN software using desktop icon, Be patient, seemingly nothing happens for several 10s of seconds. Finally the splashscreen appears. Select "ZEN system" to connect to the microscope. Again, wait until the system initialises and the ZEN UI (see below) appears. &mdash; <span style="background-color:orange;color:ghostwhite;border-radius:50px;">&nbsp;5&nbsp;</span></li>
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
</details>
<details>
  <summary>{{< icon "chevron-down" >}} Zen Overview</summary>

#### <span style="background-color:slategray;">&nbsp;Zen Overview&nbsp;</span>
As detailed in the figure below, the acquisition controls placed in the left third of the screen, the image windows are in the middle half of the screen, with image display controls situated underneath the image. Finally, the image saving and project controls are on the far right of the screen.
{{< figure src=ZenOverview.png 
	default=true
	caption="Zen Workspace default UI"
	class="center" >}}
</details>
<details>
  <summary>{{< icon "chevron-down" >}} Place your sample on the stage</summary>

#### <span style="background-color:slategray;">&nbsp;Place your sample on the Microscope&nbsp;</span>
This confocal microscope uses an AxioImager.Z1 stand. It has a fixed position stage, focusing moves the lens up or down. It has a manually rotating objective lens turret. To accommodate samples of different sizes the entire lens moves from a "load" position, far away from your sample, to an "imaging" position, with the front lens near your sample. Moving from the load to the imaging positions is achieved by rotating the big black knob on the front of the microscope, near the lens turret. --- <span style="background-color:orange;color:black;border-radius:50px;">&nbsp;6&nbsp;</span>
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
</details>
<details>
  <summary>{{< icon "chevron-down" >}} Locate your sample</summary>

#### <span style="background-color:slategray;">&nbsp;Locate Your Sample&nbsp;</span>
The next part of the procedure, focusing your sample, is the trickiest bit at first. Without experience, this is the step where you will struggle. **With upright microscopes, it is very easy to lower the lens enough while focusing that you focus through your sample, without seeing it, breaking the slide.** Perseverance and practice are the keys to feeling at one with the microscope. Perhaps the inspiration behind the name of Zeiss' acquisition software --- ZEN.
While you are viewing the sample through the eyepieces, it can be helpful to have the "locate" tab selected in the software to see the status of the microscope hardware and to open/close shutters, *et cetera*.
{{< columns >}}
1. Place your sample on the stage, coverslip facing up.
1. Select the a lens and rotate it into position using the silver wheel found at the top of the lens turret. 
1. Depending on the lens you are using, make sure you have used the appropriate immersion media placed on top of your sample.
1. Lower the lens into the imaging position using the black rotating knob. --- <span style="background-color:orange;color:black;border-radius:50px;">&nbsp;6&nbsp;</span>
{{< alert  >}}
Do this slooooowly. The lens may lower and crush your sample, depending on the last users' settings.{{< /alert >}}
1. If using immersion media, focus the lens until it makes contact with the media.
1. Using the "Locate" tab in the software, activate the contrast method you will use to focus. This is usually a transmitted light mode or DAPI fluorescence. Press the appropriate button to turn on the light. --- <span style="background-color:orange;color:ghostwhite;border-radius:50px;">&nbsp;7&nbsp;</span>
	- BF: Brightfield
	- Dapi: Blue Fluorescence
	- GFP: Green Fluorescence
	- RFP: Red Fluorescence
	- OFF: Off
1. Check that the light path will send the light to the eyepieces and not the confocal scanhead.
1. ***Carefully***, while looking through the lens, ***slowly*** lower the lens to focus your sample.

{{< alert cardColor="#e63946" >}}
**Warning!** This action is can be destructive!
{{< /alert >}}

{{< alert icon="circle-exclamation" cardColor="#f57e42" >}}
**It's easy to focus through your slide and break it!**
{{< /alert >}}

9. Use the joystick on the stage controller to find an appropriate field of view.
9. You are done with the microscope. Move the reflector turret to an open position (position 4 or 5), and change the ligthpath selector to direct the transmitted light or the emitted fluorescence light to the scanhead.
{{< column >}}
{{< figure src=locateTab.png
	default=true
	width=400px
	class="center" >}}
{{< endcolumns >}}
</details>
<details>
  <summary>{{< icon "chevron-down" >}} Configure the Acquisition</summary>

#### <span style="background-color:slategray;">&nbsp;Configure the Acquisition&nbsp;</span>
The easiest way to get started is to tell the confocal which set of fluorophores you have in your sample and let the system configure all the optical components.
{{< columns >}}
1. Switch to the Acquisition tab. --- <span style="background-color:orange;color:ghostwhite;border-radius:50px;">&nbsp;8&nbsp;</span>
1. Click the "Smart Setup" button. --- <span style="background-color:orange;color:ghostwhite;border-radius:50px;">&nbsp;9&nbsp;</span>
1. This will open the smart setup pane
{{< figure src=smartSetup.svg
					default=true
					class="center" >}}
1. Add a channel by clicking the "+" button. --- <span style="background-color:orange;color:ghostwhite;border-radius:50px;">&nbsp;11&nbsp;</span>
1. This opens the "Add a dye or contrasting method" pane. --- <span style="background-color:orange;color:ghostwhite;border-radius:50px;">&nbsp;12&nbsp;</span>
{{< figure src=smartSetup.svg
					default=true
					class="center" >}}
1. From this window, select the set of dyes in your sample. The system will configure the light path to optimize image data acquisition.
1. Once all the dyes are selected, close the add a dye pane.
1. The smart setup pane will now be populated with your dye choices and you must make several decisions about how you would like to image this set of dyes.
	1. Choose either LSM (Confocal) or Airyscan (SR -- Super Resolution)
	1. Choose Fastest, Best Signal, or Smartest (Line)
		- Fastest --- Fastest, but most prone to bleed-through/emission cross-talk.
		- Best Signal --- Least amount of emission cross-talk at the expense of time.
		- Smartest (line) --- The best of both worlds, have your cake and eat it, too.
	1. Best Practice --- Always choose "Best Signal" when you have fixed samples. 
{{< column >}}
{{< figure src=drawing.svg
					default=true
					class="center" >}}



</details>
<details>
  <summary>{{< icon "chevron-down" >}}Start Imaging</summary>

#### <span style="background-color:slategray;">&nbsp;Start scanning to collect image data&nbsp;</span>
{{< columns>}}
Three toggle buttons in the acquisition tab control the scanning. Clicking on them starts scanning, clicking again stops the scanning.
- **Live**
  - Scans as fast as possible. Uses a 512x512 array, fastest scan speed, no averaging. Only scans the track that is highlighted in the Channels panel. You can switch between tracks while Live by selecting the track in the Channels panel.
- **Continuous**
  - Uses the settings defined in the **Acquisition Mode** panel. Using this setting, you can see how the arry size or the averaging will affect the quality and speed of data collection.
- **Snap**
  - Takes an image of all the ticked tracks in the **Channels** panel with settings defined in the **Acquisition mode** panel.
{{< column >}}
{{< figure src=acquisitionTab.svg
					default=true
					class="center" >}}
{{< endcolumns >}}

</details>
<details>
  <summary>{{< icon "chevron-down" >}} Optimise your images</summary>

#### <span style="background-color:slategray;">&nbsp;Optimise each channel&nbsp;</span>
Typically, a fluorescence image is composed of several individual channels. For example, you may have labelled your sample with DAPI, Alexa 488, and Alexa 568. This is a typical multicolour imaging experiment. To create a quantitative, high-quality image, several important properties of each channel need to be optimised prior to acquiring the final 3-colour dataset.
 - The pixel size (pixel dimensions) --- this impacts the spatial resolution of the image
 - The range of intensity values in the image --- this impacts, the ability to separate the things in the image you care about from the things you don't care about.
 - The variability of the intensity values in the image --- this impacts the visual quality of the image, as well as the ability to extract useful quantitative information from the image.

<h4>Pixel Size</h4>
<h5>TL;DR</h5>
Press the "optimal" button to set the appropriate pixel size.
 <p>&nbsp;</p>
<h5>The background</h5>
The pixel size needs to be optimised for one channel and then held constant for the other channels. The final dataset consists of the  individual channel images displayed simultaneously. To overlay the channels, such that they line up with each other, the pixel dimensions of each channel must be identical. Therefore, optimise the pixel size for one channel and subsequently hold this value constant.
To understand image optimisation, the way in which a confocal microscope forms an image is important to comprehend. In a point-scanning confocal microscopes, the image is constructed pixel by pixel. The instrument focuses a laser beam on a single point of a specimen at a time and moves the spot laterally across the sample in a raster pattern (by convention, these are  referred to as the X and Y dimensions) to build a complete 2D picture. As the beam sweeps across the sample from left to right, fluorescence is induced at each spot and collected by point detector -- a photomultiplier tube that converts the # of photons emitted from each spot into numbers that can be stored in the computer. At the end of each X line, the laser beam is momentarily switched off while the scanning system resets the spot back to the left side of the image, one pixel down in the Y-direction. The beam is switched back on and line 2 is collected as the beam again moves across the sample from left to right. This is repeated until the required number of lines collected is reached.  
{{< figure src=raster.svg
		caption="The raster scanning pattern that the laser beam takes in the focal plane to create a 2D image." 
>}}
</details>

<details>
  <summary>{{< icon "chevron-down" >}} Turn OFF the system</summary>

#### <span style="background-color:slategray;">&nbsp;Turn OFF the Microscope&nbsp;</span>
After you are finished with your imaging session, please shut down the microscope. If there is another user starting a session within 30 minutes of the end of your session, leave all the hardware on. In this case, just save your images and exit from ZEN. If the time between imaging sessions is more than 30 minutes, then turn everything off to give the system a rest. Essentially, you follow the turning on instructions in reverse order. 
1. Save Images and Exit ZEN.
1. Remember to transgfer your data to the research data storage (RDS) network shared storage and REMOVE it from the acquisition conmputer.
1. Remove your sample from the stage and clean any immersion media from the lens using lens tissue.
1. Use the Windows Start menu to shut down the acquisition computer.
1. Shut off the HXP --- Fluorescence light source --- lamp.
1. Turn off the lasers by turning the key on the laser module.
1. Turn off the Components and System switches on the PSU module.
1. Turn off the power to the system by switching off the three power sockets, two for the microscope and one for the HXP lamp, at the wall.
1. 
</details>