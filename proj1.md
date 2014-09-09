---
layout: default
title: Project 1 -- Photo Alignment & Colorization
permalink: proj1/index.html
---

<style type="text/css">
img {
    max-width: 150px;
    border: 1px solid #CCC;
    border-radius: 4px;
}
</style> 

# Project 1

## Colorizing the Prokudin-Gorskii Photo Collection

## Background
To create the images below, I followed a simple process:

* Split The original image into thirds
* When Aligning I disregard 5% on each side to get around misaligned borders
* The images shift through a [-10 10] window on the X and Y axis and use the NCC formula to try to achieve a maximum alignment value.
* For large images I implemented a very basic pyramid technique using `imresize` which recursively scales images to try to optimize alignment of big files. Currently with NCC most large images complete in a little under 20 seconds. 

You can see that for most images NCC works decently, however, it is far from a perfect metric.  Unfortunately, I didn't have much time to implement many extras.

You can click on each image for the full size output.

## Example Images NCC

* Green Shift [-3 2]
* Red Shift [9 0]
[![result-monastery](result-monastery.jpg)](large-result-monastery.jpg)


* Green Shift [7 0]
* Red Shift [15 -1]
[![result-settlers](result-settlers.jpg)](large-result-settlers.jpg)


* Green [1 2] 
* Red [8 3]
[![result-cathedral](result-cathedral.jpg)](large-result-cathedral.jpg)


* Green Shift [3     2]
* Red Shift [6     3]
[![result-tobolsk](result-tobolsk.jpg)](large-result-tobolsk.jpg)


* Green Shift [59    15]
* Red Shift  [122    13]
[![result-harvesters](result-harvesters.tif)](large-result-harvesters.tif)


* Green Shift [11    17]
* Red Shift [112       -1046]
[![result-emir](result-emir.tif)](large-result-emir.tif)


* Green Shift [53    12]
* Red Shift [113    10]
[![result-three_generations](result-three_generations.tif)](large-result-three_generations.tif)

 
* Green Shift [13   -10]
* Red Shift [68     4]
[![result-bridge](result-bridge.tif)](large-result-bridge.tif)

 
* Green Shift [56    19]
* Red Shift [116    28]
[![result-turkmen](result-turkmen.tif)](large-result-turkmen.tif)


* Green Shift [49     8]
* Red Shift [124     9]
[![result-lady](result-lady.tif)](large-result-lady.tif)


* Green Shift [40     4]
* Red Shift [88    31]
[![result-train](result-train.tif)](large-result-train.tif)


* Green Shift [51    26]
* Red Shift [108    36]
[![result-onion_church](result-onion_church.tif)](large-result-onion_church.tif)


* Green Shift [82     7]
* Red Shift [178    12]
[![result-melons](result-melons.tif)](large-result-melons.tif)


* Green Shift [76    26]
* Red Shift [173    34]
[![result-selfie](result-selfie.tif)](large-result-selfie.tif)


* Green Shift [18     0]
* Red Shift [137    22]
[![result-village](result-village.tif)](large-result-village.tif)
