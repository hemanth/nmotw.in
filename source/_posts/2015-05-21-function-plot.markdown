---
layout: post
title: "function-plot"
date: 2015-05-21 13:51:06 +0000
comments: true
categories: graphs, util
---

#[function-plot](http://npm.im/function-plot/)
> A simple 2d function plotter powered by d3

function-plot helps to render functions with little configuration think of it like a util that would help you to render something like what Google does. [y = x * x](https://www.google.com/webhp?sourceid=chrome-instant&ion=1&espv=2&es_th=1&ie=UTF-8#q=y+%3D+x+%5E+2)

The library currently supports interactive line charts and scatterplots, whenever the graph scale is modified the function is evaluated again with
the new bounds, result: infinite graphs!


__Get it__ : `npm install --save function-plot`


__Sample usage:__

```js
var d3 = window.d3
var functionPlot = require('function-plot');
functionPlot({ /*Pass in the options*/ });
```

Check out the [options](https://github.com/maurizzzio/function-plot#instance--functionplotoptions)!

__GIF FTW!__

![function-plot](/images/function-plot/function-plot.gif)

