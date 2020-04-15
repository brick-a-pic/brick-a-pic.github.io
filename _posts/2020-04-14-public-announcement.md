---
layout: default
title: March Progress Update 
date: 2020-04-14 11:15:35 -0000
categories: information
---

## Launching Brick-a-Pic

### Introduction

Welcome to the Brick-a-Pic project! After our 5 months of development, we’d like to announce this project to the world at large. Brick-a-Pic is a web application that intends to make it as easy as possible for people to make mosaics out of LEGO bricks. If you’d like to learn more about it, read on. If you want to try it out, you can here: https://brick-a-pic.github.io/brick-a-pic/



### Running

You can try Brick-a-Pic right here, as a static site hosted on GitHub Pages. If you’d like to run your own copy, you can build it with npm, or run it as a Docker container [link to Docker instructions here]. Since it works entirely offline after the first page load, you can also save it as a progressive web application.


## Key Features

### Size Selection: 

The user can then customize the dimensions of the image to fit their desired resolution and size by either changing the slider position or directly enter the dimensions themselves. When “Preserve aspect ratio” is checked, the image retains its proportions as it is scaled.

![](/assets/img/sizeselection.gif)

### Color Quantization:

Depending on the size of their Lego collection, the user may want to check more or fewer of the colors to include, but we start with the 17 most common colors. More colors means a more realistic image, but they might be harder to find.

![](/assets/img/colorquantization.gif)


### Pan/Zoom Functionality

Once you've uploaded an image, it can be panned and zoomed across the screen at will. It's fully touch-screen compatible, too!

![](/assets/img/panzoom.gif)


### Image Size Detection / Scaling

The app will also automatically detect the relative shape of an image, and size the mosaic to match:

![](/assets/img/dimdetect.gif)
