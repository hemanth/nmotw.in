---
layout: post
title: "resize-observer-polyfill"
date: 2016-10-06 17:06:53 +0000
comments: true
categories: polyfill
---

#[resize-observer-polyfill]()
> A polyfill for Resize Observer API.

Implements event based tracking of changes in the dimensions of elements. 

Uses MutationsObserver and falls back to an infinite dirty checking cycle if the first one is not supported. 

Handles long running CSS transitions/animations, attributes and nodes mutations along with changes made by :hover pseudo-class (optional).

Compliant with the [spec](http://rawgit.com/WICG/ResizeObserver/master/index.html). 

Doesn't contain any publicly available methods except for those described in the spec. 


__Get it:__

```js
npm install --save resize-observer-polyfill
```

__Sample usage:__


```js
import ResizeObserver from 'resize-observer-polyfill';
 
const observer = new ResizeObserver((entries, observer) => {});
 
observer.observe(document.body);
```

__GIF FTW!__

![resize-observer-polyfill](/images/resize-observer-polyfill/resize-observer-polyfill.gif)


P.S: Checkout the [Live demo](http://que-etc.github.io/resize-observer-polyfill).