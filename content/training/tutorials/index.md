+++
title = 'QuPath Tutorials'
layout = 'simple'
+++

These videos show a complete whole-slide analysis workflow in [QuPath](https://qupath.github.io/), free open-source software for bioimage analysis. They were created by Maros van den Bergh. For questions, contact the [facility manager](mailto:stephen.ogg@kcl.ac.uk). The [QuPath documentation](https://qupath.readthedocs.io/en/stable/) describes each step in detail.

**Total running time: about 3 h 20 min.** Watch in order; each video builds on the previous one. [QuPath version used: 0.7.0.]

| # | Video | Length | What you learn |
|---|---|---|---|
| 1 | Setting up QuPath | 9:51 | Create a project, import images, build a composite training image to compare classifiers across slides. |
| 2 | Cell detection | 10:19 | Detect nuclei in the DAPI channel and expand them to estimate cell boundaries. |
| 3 | Cell classification | 21:14 | Classify detected cells by marker expression. |
| 4 | Pixel classification | 24:13 | Separate tumour from stroma with a trained and a threshold-based pixel classifier. |
| 5 | Pixel classification: fibroblast-like cells | 6:56 | Build a classifier from the pericyte marker channel. |
| 6 | Putting it all together | 1:03:35 | Combine classifiers; export cell density, distance and mean-intensity measurements. |
| 7 | Excel pivot tables: cell density | 14:16 | Correct annotations, then start a pivot-table analysis. (Lightly edited.) |
| 8 | Excel pivot tables: cell distance | 48:19 | Analyse cell distances from the exported measurements. |

## 1. Setting up QuPath
{{< youtubeLite id="wqqUbFMWnfQ" label="Setting Up QuPath" title="Setting Up QuPath" >}}

## 2. Cell detection
{{< youtubeLite id="1QtzvSjhlMI" label="Cell Detection" title="Cell Detection" >}}

## 3. Cell classification
{{< youtubeLite id="e5cHvbcYd_8" label="Object Detection" title="Cell classification" >}}

## 4. Pixel classification
{{< youtubeLite id="Cixqss2xCuQ" label="Pixel Classification" title="Pixel Classification" >}}

## 5. Pixel classification: fibroblast-like cells
{{< youtubeLite id="kpXz58pG7nQ" label="Another Pixel Classification" title="Pixel Classification for fibroblast-like cells" >}}

## 6. Putting it all together
{{< youtubeLite id="8O_ARmQN6WU" label="Putting it All Together" title="Putting it All Together" >}}

## 7. Excel pivot tables: cell density
{{< youtubeLite id="A53eZm4EzIw" label="Cell Density Analysis with Excel" title="Cell Density Analysis with Excel" >}}

## 8. Excel pivot tables: cell distance
{{< youtubeLite id="dds5JWdU7y0" label="Cell Distance Analysis with Excel" title="Cell Distance Analysis with Excel" >}}

## Good practice

- Work on **copies** of your whole-slide images, in a project stored on RDS.
- Check classifier results by eye on several slides before batch processing.
- Record software version, classifier files and settings with your results.
- Slides with uneven fluorescence tiling should be [shading-corrected](/protocols/shading-reference) first.
