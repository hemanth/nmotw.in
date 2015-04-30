---
layout: post
title: "color-string"
date: 2015-04-30 13:33:09 +0000
comments: true
categories: css color
---

[color-string](https://www.npmjs.com/package/color-string)
> Parser and generator for CSS color strings!

A module by [Heather Arthur](https://github.com/harthur) helps us to generator and parser CSS color strings.

The API names are pretty self explainatory, the module has the below methods:

__Methods for parsing:__

* getRgba

* getHsla 

* getRgb 

* getHsl 

* getHwb

* getAlpha

__Methods for generating:__

* hexString

* rgbString

* rgbaString

* percentString

* percentaString

* hslString

* hslaString

* hwbString 

* keyword


__Install it:__ `npm install --save color-string`

__Sample usage:__

```js
var colorString = require('color-string');

colorString.getRgb("#FFF")  // [255, 255, 255] 

colorString.keyword([255, 255, 0])       // "yellow" 
```
__GIF FTW!__

![color-string](/images/color-string/color-string.gif)
