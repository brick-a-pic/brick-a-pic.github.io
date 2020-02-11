--- 
layout: default
title: Project Vision
date: 2020-02-10 21:11:00 -0000
categories: information
--- 

Welcome to the Brick-a-Pic project!

We would like to announce that we are beginning development of a free, open-source, LEGO mosaic maker. Our goal is to create a web application that allows anyone to render images into mosaics made of LEGO bricks, and then create them in real life. The most recent working build of this app can be found [here](https://brick-a-pic.github.io/brick-a-pic/), and If you'd like to follow development or even contribute a pull request or issue, [our GitHub page can be found here](https://github.com/brick-a-pic/brick-a-pic).

## Motivation

Building a real-life Lego mosaic is tedious and error-prone. Brick-a-Pic aims to automate much of this process by handling the rasterization of the image into hypothetical LEGO bricks and providing instructions detailing which bricks to use and where to put them. The goal is to let a user focus on actually building their mosaic, instead of keeping track of what goes where.

## Related Work

In order to get an idea of how this project could improve upon things that already existed, we looked at some of the other applications out there that aimed to perform a task similar to this project's: [Legoizer](https://sailorhg.github.io/legoizer/), [Bricks Camera](https://apps.apple.com/us/app/bricks-camera/id1194489616), [POPMosaic.fun](https://popmosaic.pythonanywhere.com/), and [Brick-a-pic](https://www.brickapic.com/) (no relation to this project).

The upshot of this research is that we knew we wanted to focus on a LEGO mosaic-maker that provided detailed instructions for free, since it didn't seem like a comprehensive solution existed yet. The current goal is to publish a web app, so it could be easily used and shared across multiple platforms. If possible, it should do all processing client-side, to further simplify hosting to any static web server (like it is, currently).

## Technology Stack

Based on what we knew this project should accomplish, we looked at the tools we could use to this end.

**Front-End Development**

Since we decided to create a web application, a UI development framework seemed necessary to make it easy to create the interface. We decided on [Vue.js](https://vuejs.org), since it had the most familiarity among our current team members and didn't have as steep of a learning curve as other frameworks like [AngularJS](https://angularjs.org/), for the team members that needed to pick it up.

**Image Manipulation** 

We anticipate Brick-a-Pic will involve nontrivial image manipulation -- there's the problem of rasterizing arbitrary images into lower resolutions while still keeping them recognizable, and since [LEGO only consistently manufactures 17 colors](https://brickarchitect.com/2018/lego_colors/#common_colors), image colors may have to be heavily quantized. Since the current goal is to keep all image processing client-side, any and all image manipulation will have to be done in Javascript, in the browser. Thus, we looked at Javascript libraries that could help with that -- [Camanjs](http://camanjs.com/), [glfx](https://evanw.github.io/glfx.js/), [Jimp](https://www.npmjs.com/package/jimp), and the [HTML5 Canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) itself.

We came to the conclusion however, that with the presence of Canvas API calls like [getImageData](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/getImageData) and [drawImage](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/drawImage), to try to develop image manipulation routines with just the HTML5 Canvas, to reduce the number of unnecessary dependencies used.

**Containerization** 

A secondary goal of this project is to allow for multiple distribution options -- in theory, since a web app should be simple to reproduce and rehost. In order to simplify this process, our current plan is to [provide a Dockerfile](https://github.com/brick-a-pic/brick-a-pic/blob/master/Dockerfile) so that anyone can and host their own personal Brick-a-Pic instance.

## UI Mockups

In order to get an idea of what the process of using Brick-a-Pic could look like, we created mockup of a final mobile UI.

![Roughly sketched flow chart detailing user flow of Brick-a-Pic app](/assets/img/roughmockup.png)

## Future Goals

Since we are starting this project for our Open-Source Software Development course, we've developed some goals for a Minimum Viable Product (MVP) that we will create by the end of the semester (around early April, 2020).  We've also identified a list of features that would be useful and interesting to implement if time permits, given the tight schedule, but which aren't immediately critical.

### MVP Goals

* The user can select an image from their device, or take a new one
* The user can specify the final 'resolution' (in LEGO bricks) of the mosaic
* Image pixels will be reduced to the common LEGO colors that they are closest to
* The transformed image will be displayed with a LEGO overlay and grid numbering, to help with building

### Aspirational Goals

* Brick-a-Pic should work offline, as a progressive web app
* Sample images should be available for user testing
* Images can be set to use LEGO plates, which are 1/3rd the height of a normal brick, for higher-resolution results
* Mosaics have a row-by-row breakdown to make construction easier
* User can zoom/pan around the image with their mouse
* User can save/print their finished image
* More processing of the image for a better result: edge detection, computer vision, etc.—May require a backend
