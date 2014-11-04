---
layout: default
title: Project 6 -- Light Fields
permalink: proj6/index.html
---

<style type="text/css">
img {
    max-width: 350px;
    border: 2px solid #CCC;
    padding: 2px;
}
</style>

# Project 6

### Michael Ball
### cs194-ft

## Light Fields

Note: Click on all images to view the full size version!

# Basics

The basics of light field photography is surprisingly straightforward! Instead of simply capturing an image, we need to capture a bunch of images in varying locations. These multiple images allow us to reconstruct the scene by shifting the focal plane, shifting focus distance, or adjusting the aperture – all after the original image is taken. In practice, a light field camera accomplishes this by using an array of 'microlenses', however, our project was a bit more...simple. We simply used a 17x17 grid of images and reconstructed new images by cleverly closing which images we want to average. See below for some results.

---

# Examples
## Part 1: Depth Refocusing
To implement depth refocusing, we take our set of images and "shift" them to align with the center image. However, as part of the shift, we multiply the shift amount by some parameter, `a`, which allows us to adjust the equivalent focus distance. A small parameter, or `0`, is the equivalent of focusing at the far end of the scene, which a larger parameter is equivalent to focusing on nearby objects. These examples illustrate the chess board piece.

* Parameter: `0`, far distances:
    [![Chess A0](chess%20A0.png)](chess%20A0.png)

* Parameter `1.5`:
    [![Chess A15](chess%20A15.png)](chess%20A15.png)

* Parameter `3`:
    [![Chess A3](chess%20A3.png)](chess%20A3.png)

* Animated GIF:
    [![ChessFocus](chessFocus.gif)](chessFocus.gif)

---
## Part 2: Aperture Adjustment
Aperture Adjustment follows a similar technique to part 1. However, our parameter becomes the `radius` of our aperture. Instead of controlling the shift amount, the radius controls which images we chose to keep in the averaged file. A small `radius` is equivalent to a small aperture, and uses the fewest number of image files to average. This will usually produce a blurrier result, akin to a photo with a shallow depth of field.

* `Radius`: 1
    [![Chess R0](chess%20R0.png)](chess%20R0.png)

* `Radius`: 5
    [![Chess R5](chess%20R5.png)](chess%20R5.png)

* `Radius`: 10
    [![Chess R10](chess%20R10.png)](chess%20R10.png)

* Animated GIF:
    [![ChessAperture](chessAperture.gif)](chessAperture.gif)
    

---
# **Bells And Whistles**
I took my own images on a 6x6 grid using a tripod and a nodal rail. The horizontal movement was 1mm across and the vertical movement was 1mm down. However, it is hard to accurately move the vertical column in my tripod because it isn't geared...ah, well... The horizontal movement was easy to control, because the rail I was using and the camera plate have markings. 

Subject: The subject is a gigantic Rhinovirus (blue) and Epstien-Barr disease. These microbes are the common cold, and mono. 

I used my Canon 5D Mark III and scaled all photos to 15% the original resolution.

As you can see, the results don't turn out too great, likely because the camera was shifted around too much.

Setup:

[[Camera Setup](setup.jpg)](setup.jpg)

RESULT:

FOCUSING:
Parameters: 0 to 3, with a step of 0.33
[![MicrobesApertureStack](microbesFocus.gif)](microbesFocus.gif)

Aperture Adjustment: Radius 0 to 10
[![MicrobesApertureStack](microbesApertureStack.gif)](microbesApertureStack.gif)

Due to space constraints, I couldn't upload the individual files to show the differences....

