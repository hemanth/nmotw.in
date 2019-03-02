---
layout: post
title: "scroll-into-view-if-needed"
date: 2019-03-02 23:25:04 +0530
comments: true
categories: DOM util
---

#[scroll-init-view-if-needed](https://www.npmjs.com/package/scroll-into-view-if-needed)
> Element.scrollIntoView ponyfills for things like "if-needed" and "smooth".

![scroll-into-view-if-needed](/images/scroll-into-view-if-needed/scroll-into-view-if-needed.png)

This is a ponyfill for `Element.scrollIntoViewIfNeeded`. Since then the CSS working group have decided to implement its features in `Element.scrollIntoView` as the option `scrollMode: "if-needed"`. Thus this library got rewritten to implement that spec instead of the soon to be deprecated one.

Don't miss the [Demo](https://scroll-into-view-if-needed.netlify.com).

__Get it:__ `npm install scroll-into-view-if-needed`

__Usage:__

```js
// es6 import
import scrollIntoView from 'scroll-into-view-if-needed';

const node = document.getElementById('hero');

scrollIntoView(node, {
  scrollMode: 'if-needed',
  block: 'nearest',
  inline: 'nearest',
})

scrollIntoView(node, { block: 'center', inline: 'center' });
// scrollMode is "always" by default

// smooth scroll if the browser supports it and if the element isn't visible
scrollIntoView(node, { behavior: 'smooth', scrollMode: 'if-needed' });
```

__GIF FTW!__

![scroll-into-view-if-needed](/images/scroll-into-view-if-needed/scroll-into-view-if-needed.gif)

