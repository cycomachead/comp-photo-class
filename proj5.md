---
layout: default
title: Project 5 -- Face Morphing
permalink: proj5/index.html
---

<style type="text/css">
img {
    max-width: 350px;
    border: 2px solid #CCC;
    padding: 2px;
}
</style>

# Project 5

 ### Michael Ball
 ### cs194-ft

## Face Morphing

Note: Click on all images to view the full size version!

# Basic Algorithm

My basic algorithm fallowed almost exactly the slides and assignment. I took a set of manually defined control pointed and then (for two images) I averaged those points and created a Delaunay triangulation. To warp an image I made an inverse warping from a weighted triangulation to the Delaunay triangulation.  
I didn't directly create an affineTransformation but used the same technique within the main loop to iterate over the triangles. The tricky part for me was using `interp2` and separating by color channel.

Unfortunately I have a bug where somewhere along the line, my code stopped converting the bottom parts of the image. I'm not sure what went wrong...
---

# Examples


---
# Music Video
This is a video of all the CS10 TAs

<iframe width="560" height="315" src="//bit.ly/1wuj8GU" frameborder="0" allowfullscreen></iframe>

<iframe title="YouTube video player" type="text/html"
width="640" height="390" src="//bit.ly/mballcs10tamoph"
frameborder="0" allowFullScreen></iframe>
---


---


---

---
