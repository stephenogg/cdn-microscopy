+++
date = '2025-08-29T09:39:42+01:00'
draft = false
title = 'AxioscanZ1'
layout = 'simple'
showHero = true
heroStyle = 'background'
+++
## Overview
- High Speed Brightfield and Fluorescence Slide Scanner.
- Able to perform fluorescence or colour imaging of whole slides automatedly. 
- Fluorescence Specifications:
    - 7 high powered LED light source [Zeiss Colibri](EN_product-info_Colibri-7_rel1-0.pdf) for fluorescence excitation:
        - 385nm, 430nm, 475nm, 511, 555nm, 590nm, 630nm
    - Archetypical dye examples for each LED wavelength:
        - DAPI, CFP, Alexa488, YFP, Alexa546, Alexa594, Cy5
    - Fluorescence Filter Cubes:
        - [Fs38 (GFP)](https://www.micro-shop.zeiss.com/en/uk/shop/filterAssistant/filtersets/489038-9901-000), [Fs43 (DsRed)](https://www.micro-shop.zeiss.com/en/uk/shop/filterAssistant/filtersets/489043-9901-000), [Fs50 (Cy5)](https://www.micro-shop.zeiss.com/en/uk/shop/filterAssistant/filtersets/488050-9901-000), [Fs96 (BFP)](https://www.micro-shop.zeiss.com/en/uk/shop/filterAssistant/filtersets/489096-9100-000)
    - Lenses:
        - 2.5X/0.05, Fluar 5X/0.25, Plan-Apochromat 10x/0.45, Plan-Apochromat 20x/0.8, Plan-Apochromat 40X/0.95 Corr
    - Cameras:
        - Zeiss [AxioCam506 mono](EN_product-info_Axiocam-506_mono.pdf)







## SOP
Wholeslide scanning requires a different mindset than *normal* fluorescence imaging. When imaging at a confocal, the user has complete control over the parameters required to acquire an image. The goal for whole slide imaging is to offload the entire decision making process to the system. Users should be able to load the slides, select a file (Zeiss calls this a scan profile) that contains all the instructions to complete a scan, perform a preview scan, and then press the **scan** button. The system will then scan all the slides, freeing the user to perform other tasks.
{{< columns >}}
To accomplish this, the system needs to know basic things about the imaging, like:
1. What type of contrast method you wish to use
2. Objective Lens
3. The exposure time
4. What to call the file
5. Where to store the file

{{< column >}}
Additionally and specifically for slide scanning, the system needs to know:

6. Which part of the slide contains your sample, which part of the sample you wish to scan.
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

In the Zeiss Zen slide scanning software, all of these paramters are set in a file called the "scan profile". Each sample type will require its own scan profile where all the decisions for the sample on that slide are encoded. 



background image [{{< icon "cc-by" >}}](https://creativecommons.org/licenses/by/2.0/deed.en)