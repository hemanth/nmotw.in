---
layout: post
title: "lazy-cache"
date: 2018-03-11 21:59:26 +0530
comments: true
categories: lazy
---

#[lazy-cache](https://www.npmjs.com/package/lazy-cache)
> Cache requires to be lazy-loaded when needed.

`lazy-cache` uses native, plain-vanilla, tried and true javascript getters to call node's `require()` system for faster and safer code. (~1second to 50milliseconds)

__Get it:__ `npm install lazy-cache`

__Sample usage:__

```js
const lazyOS = require("lazy-cache")(require)('os');
console.log(typeof lazyOS)
console.log(lazyOS().arch())
```
__GIF FTW!__

![lazy-cache.gif](/images/lazy-cache/lazy-cache.gif)


