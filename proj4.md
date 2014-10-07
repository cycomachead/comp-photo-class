---
layout: default
title: Project 4 -- Seam Carving
permalink: proj4/index.html
---

<style type="text/css">
img {
    max-width: 350px;
    border: 2px solid #CCC;
    padding: 2px;
}
</style> 

# Project 4
 
## Seam Carving

Note: Click on all images to view the full size version!

# Basic Algorithm
The goal of seam carving is to produce an image of a new size which is visually very similar to the original. It differs from cropping in the sense that the all the elements of the the original image should be preserved in the new one, and from scaling because the results should look natural even when the scaling is non-uniform. (As you will see this is not always the case....)

Basically, I followed the paper and implemented a straight forward version of seam carving using the gradient as a basic energy function. I then iterated backwards over the gradient to find the best seam and would remove that seam from an image. To remove multiple seams I simple iterate, removing a single seam at a time. This is a rather slow process, but hey, it works alright.

Finally, I only implemented removing of vertical seams, (that is columns of pixels). To remove horizontal seams, I transpose the image, remove seams, then transpose it back to the original state.

All the images from this assignment, except for the first (below) are my own. They were taken at Berkeley or in San Francisco. 

Here is an example of the Cabin image which I have shrunk by 150px.

Original Cabin:
[![cabin.jpg](cabin.jpg)](cabin.jpg)

Short Cabin:
[![short-cabin.jpg](short-cabin.jpg)](short-cabin.jpg)


---

# Some Successes

Original Wheeler Hall:
[![MG5277.jpg](MG5277.jpg)](MG5277.jpg)

Shrinking by 20% achieved a decent result:
[![shrink-by-20-horizMG5277.jpg](shrink-by-20-horizMG5277.jpg)](shrink-by-20-horizMG5277.jpg)

---

Embarcadero Center:
[![MG3561.jpg](MG3561.jpg)](MG3561.jpg)

Shrunk to 50% width is surprisingly OK!:
[![shrink-by-25-vertMG3561.jpg](shrink-by-25-vertMG3561.jpg)](shrink-by-25-vertMG3561.jpg)

---

Wheeler Hall:
[![MG5277.jpg](MG5277.jpg)](MG5277.jpg)

Shrinking by 20% actually turns out OK, except for one corner:
[![shrink-by-20-horizMG5277.jpg](shrink-by-20-horizMG5277.jpg)](shrink-by-20-horizMG5277.jpg)

---

Bay Bridge:
[![MAB3337.jpg](MAB3337.jpg)](MAB3337.jpg)

33% Shrink looks fine!:
[![shrink-by-33-horizMAB3337.jpg](shrink-by-33-horizMAB3337.jpg)](shrink-by-33-horizMAB3337.jpg)

---

Protester Original:
[![MAB228.jpg](MAB228.jpg)](MAB228.jpg)

33% Shrink:
[![shrink-by-33-vertMAB228copy.jpg](shrink-by-33-vertMAB228copy.jpg)](shrink-by-33-vertMAB228copy.jpg)

---

Hearst Mining Building:
[![MG3934.jpg](MG3934.jpg)](MG3934.jpg)

Large Vertical Carve works quite well! :
[![shrink-by-33-horizMG3934.jpg](shrink-by-33-horizMG3934.jpg)](shrink-by-33-horizMG3934.jpg)

---

# Some Failures


Shrinking Wheeler Hall by 50% was a bad idea:
[![shrink-by-50-horizMG5277.jpg](shrink-by-50-horizMG5277.jpg)](shrink-by-50-horizMG5277.jpg)

Shrink the protester vertically fails:
[![shrink-by-33-vertMAB228.jpg](shrink-by-33-vertMAB228.jpg)](shrink-by-33-vertMAB228.jpg)
 
---
