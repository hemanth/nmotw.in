---
layout: post
title: "color-thief"
date: 2016-03-03 14:50:23 +0000
comments: true
categories: dom util 
---

#[color-thief](https://www.npmjs.com/package/color-thief)
>Grab the color palette or dominant color from an image!

`color-thief` helps to grab get the dominant color or the color palette from an image, this module makes use of JS, some cool math and the canvas tag to make it happen.

__Get it:__ `npm install --save color-thief`

__Sample usage:__

```js
var colorThief = new ColorThief();
colorThief.getColor(sourceImage);

/*
getColor(sourceImage[, quality])
returns {r: num, g: num, b: num}
*/
```

```js
var colorThief = new ColorThief();
colorThief.getPalette(sourceImage, 8);

/*
getPalette(sourceImage[, colorCount, quality])
returns [ [num, num, num], [num, num, num], ... ]
*/
```

__GIF FTW!__

![color-thief](/images/color-thief/color-thief.gif)
