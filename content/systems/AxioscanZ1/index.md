+++
date = '2025-08-29T09:39:42+01:00'
draft = false
title = 'AxioscanZ1'
layout = 'simple'
showHero = true
heroStyle = 'background'
+++

<details>
  <summary>{{< icon "chevron-down" >}} Overview</summary>

## Overview
The AxioScan.Z1 is designed to scan the entire tissue on a slide. Our system is equipped to scan in brightfield or fluorescence modes. The system has an in built magazine to hold 100 3" X 1" slides. Once configured, the system is able to perform automated scanning by performing a pre-scan, identifying the tissue on the slide, creating a focus map, and then performing a scan using the selected instructions including magnifiation, mode, channels, exposure time and data saving location. 

Fluorescence Specifications:
- 7 LED light source [Zeiss Colibri](EN_product-info_Colibri-7_rel1-0.pdf) for fluorescence excitation:
    - wavelengths: 385nm, 430nm, 475nm, 511nm, 555nm, 590nm, 630nm
- Fluorescence Filter Cubes:
    - [Fs38 (GFP)](https://www.micro-shop.zeiss.com/en/uk/shop/filterAssistant/filtersets/489038-9901-000)
    - [Fs43 (DsRed)](https://www.micro-shop.zeiss.com/en/uk/shop/filterAssistant/filtersets/489043-9901-000)
    - [Fs50 (Cy5)](https://www.micro-shop.zeiss.com/en/uk/shop/filterAssistant/filtersets/488050-9901-000)
    - [Fs96 (DAPI)](https://www.micro-shop.zeiss.com/en/uk/shop/filterAssistant/filtersets/489096-9100-000)
- Lenses:
    - 2.5X/0.05, Fluar 5X/0.25, Plan-Apochromat 10x/0.45, Plan-Apochromat 20x/0.8, Plan-Apochromat 40X/0.95 Corr
- Cameras:
    - Zeiss [AxioCam506 mono](EN_product-info_Axiocam-506_mono.pdf)

</details>



<details>
  <summary>{{< icon "chevron-down" >}}Acquisition SOP</summary>

## SOP
Wholeslide scanning requires a different mindset than *normal* fluorescence imaging. When imaging at a confocal, the user has complete control over the parameters to acquire an image and can instantly change these, using information in the acquired data to update the acquisition parameters. Whole slide imaging, in contrast, is completely automated. The goal is to offload the entire decision making process to the system. Users should be able to load the slides, select a file (Zeiss calls this a scan profile) that contains all the instructions to complete a scan, perform a preview scan, and then press the **scan** button. The system will then scan all the slides, freeing the user to perform other tasks.
{{< columns >}}
To accomplish this, the system needs to know basic things about the imaging, like:
1. What type of contrast method you wish to use
2. Objective Lens
3. The exposure time
4. What to call the file
5. Where to store the file

{{< column >}}
Additionally and specifically for slide scanning, the system needs to know:

6. Which part of the slide contains your sample and which part of the sample you wish to scan.
7. How to focus the sample.
{{< endcolumns >}}

{{< columns >}}
<br/>
<br/>
{{< alert icon=circle-info >}} 
Pdf to understand concepts in whole slide scanning    --->
{{< /alert >}}
{{< column >}}
<a href="axio-scanz1-application-guide.pdf"><img src="applicationGuideCover.png" alt="Application Guide" width="150px" max-width="100%" style="margin:auto"></a>
{{< endcolumns >}}

In the Zeiss Zen slide scanning software, a file called the "scan profile" contains all of the scanning information. The challenge with slide scanning is to create a robust set of scan profiles that will work for all the slides of each of your sample types. Each sample type will require its own scan profile where all the decisions for that specific type of sample on that slide(s) are encoded.
### Step by Step --- Quickstart --- TL;DR
{{< timeline >}}

{{< timelineItem icon="1" header=" " subheader="Turn on the system" badge="start here" >}}
<ul>
    <li><a href="IMG_4739.JPG">Turn on the Scanner.</a> Wait until you think the scanner is initialised.</li>
    <ul>
        <li><a href="IMG_4739.JPG">There are two separate buttons to turn on the scanner.</a> One on the front and one near the power cable on the left.</li>
        <li><a href="image1.png">The top left corner of the scanner will light up blue during initialisation and then turn green when it's ready.</a></li>
    </ul>
    <li>Turn on the Computer. Wait until the Windows desktop appears.</li>
    <li><a href="SplashChoice.png">Start the software. Wait until the splashscreen appears.</a></li>
    <li><a href="SplashChoice.png">Click on the "ZEN Slidescan" button.</a> Wait until the system initialises in the software.</li>
</ul>
{{< /timelineItem >}}

{{< timelineItem icon="2" subheader="Insert your slides" >}}
<ul>
    <li><a href="loadSlides.png">Place your slides into the slide carrier. Slide label must be near the silver clamp.</a></li>
    <li><a href="loadingAid.png">You may need to use the slide loading aid if you have many slides.</a></li>
    <li>Press the open/close button on the scanner. Wait until the door opens.</li>
    <li><a href="loadSlides.jpg">Pull open one of the trays. It doesn't matter which one.</a></li>
    <li>Place the slide carrier(s) on the tray(s), coverslip up, labels closest to you. Close the tray(s).</li>
    <li>Press the open/close button to close the door. Wait until the system auto discovers the slide carrier(s) location(s).</li>
    <li><a href="cartoon.jpg">You will see a cartoon of your slides appear in the magazine tab of the acquisition software.</a></li>  
</ul>
{{< /timelineItem >}}
{{< timelineItem icon="3" subheader="Create a Scan Preview" >}}
<ul>
    <li>Select the scan profile you wish to use. Each slide can have its own profile.</li>
    <li>Push the "Preview scan" button. Wait for the preview.</li>
    <li>Observe the previews to ensure the tissue has been identified correctly. Make any necessary modifications.</li>
    <li>Select the storage location. This will likely be your folder on the Data drive.</li>
    <li>Select the naming definition. Commonly, date + serial number.</li>
</ul>
{{< /timelineItem >}}
{{< timelineItem icon="4" subheader="Scan Your Slides" >}}
<ul>
    <li>Press the "Scan" button.</li>
    <li>Your scans will be saved to your chosen location.</li>
    <li>Remember, the acquisition computer is temporary storage.</li>
    <li>Move your image data to your RDS storage location.</li>
</ul>
{{< /timelineItem >}}
{{< /timeline >}}
</details>

<details>
  <summary>{{< icon "chevron-down" >}} Creating a scan profile</summary>

## Creating a Scan Profile
Creating a scan profile is by far the most challengin part of the slide scanning workflow. In ZEN 3.1, there are two "Wizards" that can help you through the initial steps of creating a scan profile. Briefly, the steps consist of:
1. Creating a scan profile and saving it with the first wizard.
    - This includes giving the scan profile a name, and telling ZEN some basic information about the type of scan profile you would like to create.
1. Adapting this initial scan profile so that it is specific to your sample type with the second wizard.
1. Defining the preview image parameters.
1. Using the preview image to identify tissue sections on the slide.
1. Creating a focus map.
1. Defining the scan parameters.

## Detailed Instructions
{{< timeline >}}
{{< timelineItem icon="1" subheader="Naming The Scan Profile" badge="Step 1" >}}

{{< /timelineItem >}}
{{< timelineItem icon="2" subheader="Creating a label image" badge="Step 2" >}}

{{< /timelineItem >}}



{{< timelineItem icon="3" md="true" subheader="Defining the preview image parameters" badge="Step 3" >}}
> [!TIP] Information
> For best results the red frame should cover the complete slide and some air
around the edges. This will improve identification of areas to be used for automatic shading correction for brightfield imaging. To limit the range for the tissue detection use the red
frame in the Tissue Detection Settings section in the subsequent step. Avoid
placing the red frame covers the label area of the slide.

{{< figure
    src="preview.png"
    alt="Preview Image"
    caption="Include the entire slide within the red selection rectangle"
    default="true"
    width=400
    >}}
{{< /timelineItem >}}
{{< timelineItem icon="4" subheader="Tissue identification" badge="Step 4" >}}

{{< /timelineItem >}}
{{< timelineItem icon="5" subheader="Creating a focus map" badge="Step 5" >}}

{{< /timelineItem >}}
{{< timelineItem icon="6" subheader="Defining the scan parameters" badge="Step 6" >}}

{{< /timelineItem >}}
{{< /timeline >}}


</details>
<details>
    <summary><a href="https://stephenogg.github.io/cdn-microscopy/protocols/shading-reference/">Shading Correction SOP</a></summary>
</details>