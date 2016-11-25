---
layout: post
title: "svg-captcha"
date: 2016-11-24 14:52:03 +0000
comments: true
categories: svg
---

#[svg-captcha](https://www.npmjs.com/package/svg-captcha)
>Generate svg captcha.

`svg-captcha` uses OpenType font parser and text skewing martix logic to generate random SVG captchas. 

It returns an object which has the SVG data and the text which was used to generate the same.

__Get it:__ `npm install --save captcha`

__Sample usage:__

```js
var svgCaptcha = require('svg-captcha');

// generate random text of length 4
var text = svgCaptcha.randomText();

// generate svg image
var captcha = svgCaptcha(text);

// generate both and returns an object
var captcha = svgCaptcha.create();

console.log(c);
// {data: '<svg.../svg>', text: 'abcd'}
```

__GIF FTW:__

![svg-captcha](/images/svg-captcha/svg-captcha.gif)

