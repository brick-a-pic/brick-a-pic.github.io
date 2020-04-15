---
layout: default
title: Final Announcement 
date: 2020-04-14 11:15:35 -0000
categories: information
---

## Launching Brick-a-Pic!

### Introduction

Welcome to the Brick-a-Pic project! After our 5 months of development, we’d like to announce this project to the world at large. Brick-a-Pic is a web application that intends to make it as easy as possible for people to make mosaics out of LEGO bricks. If you’d like to learn more about it, read on. If you want to try it out, you can [here](https://brick-a-pic.github.io/brick-a-pic/):



### Running

 Brick-a-Pic is hosted as a static site hosted on GitHub Pages. If you’d like to run your own copy, you can build it with npm, or run it as a Docker container. Build instruction with both npm and Docker can be found in our [README.md](https://github.com/brick-a-pic/brick-a-pic/blob/master/README.md). Since Brick-a-pic works entirely offline after the first page load, you can also save it as a progressive web application.


## Key Features


### Overview:

The interface is a simple one, with a banner along the top with the app name and links if they want to learn more. Most of the screen is a preview of the resulting Lego image, with a settings panel on the left side. The panel can be shown and hidden using the hamburger button at the top left to save space.

### Image Uploading

By clicking “Open image,” users can select any image file from their computer to upload, or take a photo if they’re on a mobile device. 

![](/assets/img/openimg.gif)

If they just want to get a sense of what the app can do, they can select one of the sample images.

![](/assets/img/sampleimg.gif)

### Size Selection: 

The user can then customize the dimensions of the image to fit their desired resolution and size by either changing the slider position or directly enter the dimensions themselves. When “Preserve aspect ratio” is checked, the image retains its proportions as it is scaled.

![](/assets/img/sizeselection.gif)

### Color Quantization:

Depending on the size of their Lego collection, the user may want to check more or fewer of the colors to include, but we start with the 17 most common colors. More colors means a more realistic image, but they might be harder to find.

![](/assets/img/colorquantization.gif)

### Grid Labelling:

The resulting image will have gridlines and grid numbering to guide builders:
![](/assets/img/coordinates.png)

### Pan/Zoom Functionality

Once you've uploaded an image, it can be panned and zoomed across the screen at will. It's fully touch-screen compatible, too!

![](/assets/img/panzoom.gif)


### Static Hosting:

Since Brick-a-Pic exists entirely in the client and all processing is done directly in the browser, very little is required to host a copy.


## Contributing

Brick-a-Pic is completely free and open source, so contributions are always welcome. You can start by reading our [CONTRIBUTING.md](https://github.com/brick-a-pic/brick-a-pic/blob/master/CONTRIBUTING.md), or by looking for open issues on GitHub.
