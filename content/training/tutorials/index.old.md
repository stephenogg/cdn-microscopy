+++
date = '2026-04-07T16:38:42+01:00'
draft = false
title = 'QuPath Tutorials'
layout = 'simple'
showHero = false
+++

Below are several videos demonstrating a workflow using [QuPath](https://qupath.github.io/), an open source whole slide image analysis program. These were created by [Maros van den Bergh](https://www.linkedin.com/in/maros-van-den-bergh-9214ba143/). Contact Maros with questions.

### QuPath Overview
QuPath is open source software for bioimage analysis.
QuPath is often used for digital pathology in research because it offers a powerful set of tools for working with whole slide images - but it can be applied to lots of other kinds of image as well. [Documentation](https://qupath.readthedocs.io/en/stable/#) for QuPath describes many of the workflow components demonstrated in the videos.

#### Setting up QuPath
<p style="color:red"> Length = 09:51</p>
Creating a project. Importing images and creating a training image that is a composite of a small region from all images in the project. Allows easy comparison of classification performance on different images.
{{< youtubeLite id="wqqUbFMWnfQ" label="Setting Up QuPath" title="Setting Up QuPath" >}}
</br>
</br>

#### Cell Detection
<p style="color:red"> Length = 10:19</p>
The first step of any classification is commonly to find all the cells. Qupath does this using the DAPI channel to ientify nuclei, then expanding the boundary of the nucleui a user defined distance. 
{{< youtubeLite id="1QtzvSjhlMI" label="Cell Detection" title="Cell Detection" >}}
</br>
</br>

#### Object Detection
<p style="color:red"> Length = 21:14</p>
Once all the cells have been identified, each cell is classified according to the type of cell it is, dependent on markers that it is labelled with.
{{< youtubeLite id="e5cHvbcYd_8" label="Object Detection" title="Object Detection" >}}
</br>
</br>

#### Pixel Classification
<p style="color:red"> Length = 24:13</p>
In this video, we use pixel classification to separate tumor from stroma areas using features in the images. Separately, we also generate a threshold based pixel classifier to separate the image into the two areas, tissue and stroma. You can use whichever works best for your situation.
{{< youtubeLite id="Cixqss2xCuQ" label="Pixel Classification" title="Pixel Classificiation" >}}
</br>
</br>

#### Another Pixel Classification for fibroblast type cells
<p style="color:red"> Length = 06:56</p>
This video uses the pericyte marker channel to show how to create a pixel classifier for fibroblast like cells.
{{< youtubeLite id="kpXz58pG7nQ" label="Another Pixel Classification" title="Another Pixel Classificiation" >}}
</br>
</br>

#### Putting it All together *Length = 1:03:35*
<p style="color:red"> Length = 1:03:35</p>
This video explains how to create the annotations/detections/objects from all the classifiers we've made in the first several videos, followed by an explanation of how to extract the numerical information required for both a cell density, distance, and mean fluorescence intensity analyses.
{{< youtubeLite id="8O_ARmQN6WU" label="Putting it All Together" title="Putting it All Together" >}}
</br>
</br>

#### Excel Pivot Table Cell Density Analysis
<p style="color:red"> Length = 14:16</p>
 The Video is mostly unedited and includes a lot of stroma/tumor annotation editing after applying the classifier, showing the tweaks needed even after automating the tissue area type detection. One section also shows how to start a pivot table analysis in excel after extracting the measurements from Qupath.
{{< youtubeLite id="A53eZm4EzIw" label="Cell Density Analysis with Excel" title="Cell Density Analysis with Excel" >}}
</br>
</br>

#### Excel Pivot Table Cell Distance Analysis
<p style="color:red"> Length = 48:19</p>

{{< youtubeLite id="dds5JWdU7y0" label="Cell Density Analysis with Excel" title="Cell Density Analysis with Excel" >}}
</br>
</br>