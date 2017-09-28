---
layout: post
title: "stikcybits"
date: 2017-07-08 15:28:28 +0530
comments: true
categories: dom util 
---

#[stickybits](https://www.npmjs.com/package/stickybits)
> Alternative to position: sticky polyfills.

* Aprox `~2KB` of javascript that would help us to know when a DOM element is stuck (position:sticky).

* It can add a CSS Sticky Class `.js-is-sticky` when `position: sticky` elements become active and a CSS Stuck Class `.js-is-stuck` when they become stuck.

* Loosely mimics `position: sticky` to consistently stick elements vertically across multiple platforms.

__Get it:__ `npm install stickybits`

__Sample usage:__


```js
 stickybits('selector', options);

 /*
Options:

    - target = el (DOM element)
    - offset = 0 || 'dealer's choice'
    - verticalPosition = top || bottom
    - useStickyClasses = true || false
    - elStyles = CSS Styles
    - positionVal = fixed || sticky
 */
```

__GIF FTW!__

![stickybits.gif](/images/stickybits/stickybits.gif)

