---
layout: post
title: "animate-css-grid"
date: 2018-12-09 09:21:40 +0530
comments: true
categories: CSS
---

#[animate-css-gird](https://www.npmjs.com/package/animate-css-grid)
> Easy transitions for CSS Grid.

`FLIP` animation applied on CSS grids with the help of `MutationObserver` that activates when the grid or one of its children adds or loses a class or element.

__Get it:__ `npm install animate-css-grid`

__Sample usage:__


```js
import { wrapGrid } from animateCSSGrid
 
const grid = document.querySelector(".grid");
const config = {
  // int: default is 0 ms
  stagger: 100,
  // int: default is 250 ms
  duration: 500
  // string: default is 'easeInOut'
  easing: 'backInOut'
};

wrapGrid(grid, config);
```

```html
<!-- grid style applied via a class -->
<ul class="some-grid-class-that-changes">
  <!-- each grid item has a single direct child -->
  <li class="grid-item">
    <div>
      <h3>Item title</h3>
      <div>Item body</div>
    </div>
  </li>
<div>
```

Check out the [DEMO](https://codepen.io/aholachek/pen/VXjOPB)!


__GIF FTW!__

![animate-css-grid](/images/animate-css-grid/animate-css-grid.gif)
