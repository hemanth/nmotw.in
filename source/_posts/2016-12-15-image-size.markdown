---
layout: post
title: "image-size"
date: 2016-12-15 15:58:47 +0000
comments: true
categories: util
---

#[image-size](https://www.npmjs.com/package/image-size)
>get dimensions of any image file

`image-size` maybe call it `image-dimensions`? Anyway it's a sweet module that does one thing and does it right! 

__Supported image types:__

* BMP
* GIF
* JPEG
* PNG
* PSD
* TIFF
* WebP
* SVG


__Sample usage:__

```
npm install image-size --save
```

__Sync:__

```javascript
var sizeOf = require('image-size');
var dimensions = sizeOf('images/funny-cats.png');
console.log(dimensions.width, dimensions.height);
```


__Async:__

```javascript
var sizeOf = require('image-size');
sizeOf('images/funny-cats.png', function (err, dimensions) {
  console.log(dimensions.width, dimensions.height);
});
```

__GIF FTW!__

![image-size](/images/image-size/image-size.gif)
