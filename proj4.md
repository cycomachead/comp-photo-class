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

_Note: Click on all images to view the full size version!_

# Basic Algorithm
The goal of seam carving is to produce an image of a new size which is visually very similar to the original. It differs from cropping in the sense that the all the elements of the the original image should be preserved in the new one, and from scaling because the results should look natural even when the scaling is non-uniform. (As you will see this is not always the case....)

Basically, I followed the paper and implemented a straight forward version of seam carving using the gradient as a basic energy function. I then iterated backwards over the gradient to find the best seam and would remove that seam from an image. To remove multiple seams I simple iterate, removing a single seam at a time. This is a rather slow process, but hey, it works alright.

Finally, I only implemented removing of vertical seams, (that is columns of pixels). To remove horizontal seams, I transpose the image, remove seams, then transpose it back to the original state.

All the images from this assignment, except for the first (below) are my own. They were taken at Berkeley or in San Francisco. 

Here is an example of the Cabin image which I have shrunk by 150px.

Original Cabin:
![[cabin.jpg](cabin.jpg)](cabin.jpg)

Short Cabin:
![[short-cabin.jpg](short-cabin.jpg)](short-cabin.jpg)


---

# Some Successes

---

# Some Failures

---
