---
layout: post
title: "wifi-triangulate"
date: 2016-07-21 17:16:26 +0000
comments: true
categories: wifi mad 
---

# [wifi-triangulate](https://www.npmjs.com/package/wifi-triangulate)
> Finds your current position on planet earth using the wifi access points in your vicinity.


This module requires that the wifi card on your computer is active and that you have access to the internet in order to communicate with Google so that it can triangulate your position.


__Get it:__ `npm install --global wifi-triangulate`

__Sample usage:__


```js
var triangulate = require('wifi-triangulate')
 
triangulate(function (err, location) {
  if (err) throw err
  console.log(location) // => { lat: 38.0690894, lng: -122.8069356, accuracy: 42 } 
})
```

__GIF FTW!:__

![wifi-triangulate](/images/wifi-triangulate/wifi-triangulate.gif)

