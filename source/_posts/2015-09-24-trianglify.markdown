---
layout: post
title: "trianglify"
date: 2015-09-24 11:53:44 +0000
comments: true
categories: svg 
---

#[Trianglify](https://www.npmjs.com/package/trianglify)
> Trianglify generates colorful triangle meshes that can be used as SVG images and CSS backgrounds.

This is inspired by [btmills/geopattern](https://github.com/btmills/geopattern) thanks to [Quinn Rohlf](http://qrohlf.com/) for this.

__Get it:__ ``` npm install --save trianglify ```

__Sample usage:__

```js
var Trianglify = require('trianglify');
var pattern = Trianglify({width: 200, height: 200});
document.body.appendChild(pattern.canvas());
```

There are few wonderful [options](https://github.com/qrohlf/trianglify/blob/master/Readme.md#options) `color_function` being one of them.

Color function that uses the HSL color format to generate a rainbow pattern:

```js
var colorFunc = function(x, y) {
    return 'hsl('+Math.floor(Math.abs(x*y)*360)+',80%,60%)';
};

var pattern = Trianglify({color_function: colorFunc})
```

__GIF FTW!__

![Trianglify](/images/trianglify/trianglify.gif)

