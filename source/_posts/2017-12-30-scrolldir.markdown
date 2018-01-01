---
layout: post
title: "scrolldir"
date: 2017-12-30 15:32:47 +0530
comments: true
categories: dom
---

#[scrolldir](https://nmpjs.org/scrolldir)
> leverage scroll direction with CSS ⬆⬇

`0` dep, `1KB` micro JS lib to easily leverage vertical scroll direction in CSS via a data attribute.

__Get it:__ `npm install scrolldir`

__Sample usage:__

```js
scrollDir();

scrollDir({ attribute: 'new-attribute-name' });

scrollDir({ el: 'your-new-selector' });

scrollDir({ off: true });

scrollDir({ direction: 'up' });
```

ScrollDir will set the `data-scrolldir` attribute on the `<html>` element to `up` or `down`.

__GIF FTW!__

![scrolldir.gif](/images/scrolldir/scrolldir.gif)
