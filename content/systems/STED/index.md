+++
date = '2026-07-15T14:39:42+01:00'
draft = false
title = 'Abberior Mirava Polyscope'
layout = 'simple'
showHero = true
heroStyle = 'background'
+++

### Mirava Polyscope

[abberior’s MIRAVA® POLYSCOPE®](https://abberior.rocks/superresolution-confocal-systems/mirava-polyscope/) combines confocal with STED to extend resolution beyond diffraction-limited imaging.

[Video Overview](https://mediaspace.epfl.ch/media/MIRAVA+Abberior/0_ostaquci) of the system and detailed explanation of the LiGHTBOX software for image acquisition made by Abberior, hosted by EPFL. One hour length.

NB - Our system does NOT have the MiNFLUX module, the MATRIX array detector or the TIMEBOW FLIM option.

[Link](https://github.com/stephenogg/cdn-microscopy/releases/tag/0.0.1) to download the software to install on your own computer. Select either the MacOS (dmg) version or the Windows installer (msi).


Our system specifications:
- IX83 Olympus motorised, inverted stand
- coolLED excitation for sample finding, focusing
- single quadband (DAPI/FITC/Cy3/Cy5) filter for wf imaging
- XYZ motorised stage. 200 micrometer z-range
- 4 excitation laser lines: 405nm, 485nm, 561nm, and 640nm
- Point Scanner with a line frequency of up to 2.6KHz.
- UPLXAPO 60X/1.42 Oil immersion lens for confocal and STED imaging (0.15mm working distance)
- Confocal resolution: ~ 250nm lateral, 750nm Z 
- 775nm STED depletion laser for 2D & 3D STED
	- 2D STED resolution: 30nm
	- 3D STED resolution: 80nm isotropic
- 3 APDs with 65% QE and dark counts < 250Hz
- RAYSHAPE adaptive optics system for all beams (excitation, emission, and depletion). Minimize spherical abberation for deep imaging.
- TRUESHARP deconvolution
- FLSEXPOSURE Adaptive illumination package for highest resolution and live-cell super-resolution imaging at ultra-low light levels (RESCue, DyMIN)

### Sample Preparation and Fluorophore Selection for STED Microscopy

#### Sample Preparation and microscope information PDF document: [Sample Prep Info](samplePrep.pdf)

In STED microscopy, sample preparation is a critical determinant of image quality and achievable spatial resolution. Unlike conventional fluorescence microscopy, where resolution is primarily constrained by diffraction, the performance of STED microscopy is frequently limited by the quality of specimen preparation, labelling efficiency, and fluorophore behaviour. Because STED imaging relies on high-intensity depletion laser irradiation to restrict fluorescence emission to sub-diffraction volumes, samples must exhibit a high signal-to-noise ratio, minimal background fluorescence, and excellent structural preservation. Consequently, fixation protocols should preserve cellular ultrastructure while maintaining antigen accessibility, and labelling strategies should provide sufficient fluorophore density to accurately represent nanoscale biological features. Inadequate fixation, low labelling efficiency, or non-specific staining can introduce artefacts that compromise both image fidelity and effective resolution.

The choice of fluorophore is particularly important in STED microscopy. Not all fluorescent probes are suitable for STED imaging, as the intense depletion beam places substantial demands on fluorophore brightness and photostability. Optimal dyes should exhibit high quantum yield, efficient stimulated emission at the depletion wavelength, and resistance to photobleaching. Organic fluorophores such as the Abberior STAR, ATTO, and Alexa Fluor dye families are commonly employed because they combine high brightness with favourable STED performance. Fluorophore selection must also consider spectral compatibility with the excitation and depletion lasers available on the microscope, as mismatches can reduce depletion efficiency and limit resolution gains. Furthermore, the effective resolution achieved in a STED image depends not only on the microscope optics but also on the size and distribution of the fluorescent label itself. Large probes or sparse labelling can become the dominant limiting factor when imaging biological structures at nanometre scales. Therefore, careful optimization of fluorophore choice, labelling density, fixation conditions, and mounting media is essential to fully exploit the super-resolution capabilities of STED microscopy.

> In STED microscopy, image quality is often limited less by the optical system than by the quality of sample preparation and fluorophore selection. Even the highest-performing STED instrument cannot recover structural information that has been lost through poor preservation, insufficient labelling, or photobleaching.


### Tutorial

##### Step by Step --- Quickstart --- TL;DR
{{< timeline >}}

{{% timelineItem icon="1" header=" " subheader="Turn **ON** the system" badge="start here" %}}

- Turn on the computer.
- Turn on the controllers.
- Turn on the Microscope Stand Touch Panel - wait until it's completely initialised.
- Login to the computer iwth your King's credentials.
- Open the LiGHTBOX Software.
- If you're first user of the day, click **Yes** when the system asks you whether you want to turn the microscope ON.

{{% /timelineItem %}}

{{% timelineItem icon="2" header=" " subheader="Focus your sample" badge="Fluorescence/Brightfield Imaging" %}}

- Select "FL" on the microscope touch panel.
- Switch the LED **ON**
- Select appropriate wavelength for LED excitation.
- Alternatively, select "BF" on the microscope controller for Brightfield imaging.
- Select the "DIA" pane to control the lamp brightness.
- Focus --- Clockwise moves the lens down.
- 

{{% /timelineItem %}}

{{% timelineItem icon="3" header=" " subheader="Find a field of view." badge="Fluorescence/Brightfield Imaging" %}}

- X/Y Stage Control: top dial moves X, bottom dial moves Y.  Third dial does nothing.
- +/- change the speed of the stage
- Press the green LED on the front of the stage (yes, it's also a button) to release the stage for manual movement.
- Press the green LED again to lock the stage and transfer control back to the dial controller.

{{% /timelineItem %}}

{{% timelineItem icon="4" header=" " subheader="Change the default save location." badge="Pre-Acquisition Setup" %}}

- From the "Welcome" hamburger menu, select "change default save location".
- Initially, the default is "C:\User\abberior\Documents\Pictures"
- Select the D: drive and sub-folder with your name. (Create your folder first, if needed.)

{{% /timelineItem %}}

{{% timelineItem icon="5" header=" " subheader="Acquisition Setup." badge="Pre-Acquisition Setup" %}}

- From the "Welcome" hamburger menu, select "change default save location".
- Initially, the default is "C:\User\abberior\Documents\Pictures"
- Select the D: drive and sub-folder with your name. (Create your folder first, if needed.)

{{% /timelineItem %}}

{{< /timeline >}}