---
layout: default
title: Project 3 -- Fun With Frequencies
permalink: proj3/index.html
---

<style type="text/css">
img {
    max-width: 300px;
    border: 2px solid #CCC;
    padding: 2px;
}
</style> 

# Project 3
### (Not So much :( ) Fun With Frequencies

Click on all images to view the full size version!

# Part 0 -- Image Sharpening
For this part of the project, I implemented the unsharp mask technique from lecture. 

The basic technique is to take the image, then create a low-pass filtered, or blurred version. Then you take the difference of the image and the blurred version and it back to the original image. 

There are 3 examples of images I attempted to sharpen. These were all sharpened with an alpha value of 4, and a sigma of 0.75.

The first blurry image.
[![Blurry 1](blurry_1.jpg)]((blurry_1.jpg))
The sharpened result
[![Sharpened Blurry 1](sharpened-blurry_1.jpg)]((sharpened-blurry_1.jpg))


[![Blurry 2](blurry_2.jpg)]((blurry_2.jpg))
[![Sharpened Blurry 2](sharpened-blurry_2.jpg)]((sharpened-blurry_2.jpg))


[![Lady-Lena](lady.jpg)]((lady.jpg))
[![Sharpened Lady-Lena](sharpened-lady.jpg)]((sharpened-lady.jpg))

***

# Part 1 -- Hybrid Images
For this part, I implemented hybrid images using the techniques presented in class. That is, we take two images and create a "hybrid" by applying a low pass filter to one image and a high pass filter to the second. The result is that depending on the viewing distance, you will primarily notice one of the images in the composite. Low frequencies are better seen up close, and high frequencies are better seen from further away. 

The first image I tried was, of course, the hybrid of Derek and nutmeg.
[![nutmeg.jpg](nutmeg.jpg)](nutmeg.jpg)
This was the high frequency image, with F_c_ being 0.02.
[![DerekPicture.jpg](DerekPicture.jpg)](DerekPicture.jpg)
This was the low frequency image with F_c_ being 0.003.
__Result:__
[![hybrid-DerekPicture.jpg-nutmeg.jpg](hybrid-DerekPicture.jpg-nutmeg.jpg)](hybrid-DerekPicture.jpg-nutmeg.jpg)


#### iDroid
Next, I created the iDroid -- a device so conflicted, it would be dangerous to use!
[![iphone.png](iphone.png)](iphone.png)
This was the low frequency image with F_c_ being 0.03.
[![galaxy.jpg](galaxy.jpg)](galaxy.jpg)
This was the high frequency image, with F_c_ being 0.01.
__Result:__
[![hybrid-iphone.png-galaxy.jpg](hybrid-iphone.png-galaxy.jpg)](hybrid-iphone.png-galaxy.jpg)

Bonus:
I created the hybrid using a black iPhone, but I didn't like the result as much...
[![hybrid-iphone6.jpg-galaxy.jpg](hybrid-iphone6.jpg-galaxy.jpg)](hybrid-iphone6.jpg-galaxy.jpg)

#### The Unstable Tower
The final create was the Unstable tower, a mashup of the Campanile and Hoover Tower. I do not recommend you enter this building as you don't know what will happen...
[![campanile.jpg](campanile.jpg)](campanile.jpg)
This was the low frequency image with F_c_ being 0.04.
[![hootow.jpg](hootow.jpg)](hootow.jpg)
This was the high frequency image, with F_c_ being 0.005.
__Result:__
[![hybrid-hootow.jpg-campanile.jpg](hybrid-hootow.jpg-campanile.jpg)](hybrid-hootow.jpg-campanile.jpg)

For these images, I chose to create the FFT plots.
Campanile:
[![campo-fft.jpg](campo-fft.jpg)](campo-fft.jpg)
Hover Tower:
[![hootow-fft.jpg](hootow-fft.jpg)](hootow-fft.jpg)
Hybrid:
[![tower-fft.jpg](tower-fft.jpg)](tower-fft.jpg)

***
## Part 2 Gaussian and Laplacian Stacks

For this part I created Gaussian and laplacian stacks. The gaussian stacks were created by starting with a sigma value of 2 and the doubling it for each level of the stack. Each image was convolved against the original image, not the previous one. The laplacian stacks use the guassian, but at the next level of the stack, subtracted from the original image.

### Campanile
[![camp-gauss-stack.jpg](camp-gauss-stack.jpg)](camp-gauss-stack.jpg)
[![camp-laplace-stack.jpg](camp-laplace-stack.jpg)](camp-laplace-stack.jpg)

### Lincoln
[![linc-gauss-stack.jpg](linc-gauss-stack.jpg)](linc-gauss-stack.jpg)
[![linc-laplace-stack.jpg](linc-laplace-stack.jpg)](linc-laplace-stack.jpg)


***
## Part 3
Unfortunately, I was sick and ran out of time for this part.....

## Closing thoughts:
I really enjoyed making hybrid images and was disappointed I didn't get a chance to try making a pemato (pear and tomato hybrid).