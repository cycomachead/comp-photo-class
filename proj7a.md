---
layout: default
title: Project 7A -- Panoramas
permalink: proj7/index.html
---

<style type="text/css">
img {
    max-width: 350px;
    border: 2px solid #CCC;
    padding: 2px;
}
</style>

# Project 7

### Michael Ball
### cs194-ft

# Panoramas

Note: Click on all images to view the full size version!

# Basics

To create a panorama we want to warp a series of images on to one other. We first create a homography, which is a 2D transformation between 2 images based on 4 points (or more) in the image. For this project, we will manually pick the 4 corresponding points to align the images. Then we will successively warp images in the set onto a main output image, merging each image by multiplying a weight value to all the pixels so the merge looks a little cleaner. 

Unfortunately my project didn't work so well...

---

# Examples

## Rectification
To "rectify" an image we can warp one image to a homography based on 4 points and a matrix which describes coordinates to transform those points. I tried warping the 4 points in this monitor to a 16x9 rectangle. (Naturally, my project is broken....)

* Original:  [![images/warp.jpg](images/warp.jpg)](images/warp.jpg)
* Result:  [![room-rectify.jpg](room-rectify.jpg)](room-rectify.jpg)

---

## Panos
I have two panos, which both don't quite work obviously.
The source for these images in available in 

* [images/utah](images/utah/) for the Utah images (6 images)
* [images/room](images/room/) for the one on my desk (3 images)

#### Broken Results

* Utah:
    * [![pano-utah.jpg](pano-utah.jpg)](pano-utah.jpg) 
* Room:
    * [![pano-room.jpg](pano-room.jpg)](pano-room.jpg)
    
---