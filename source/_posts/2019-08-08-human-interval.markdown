---
layout: post
title: "human-interval"
date: 2019-08-08 15:21:19 +0530
comments: true
categories: util
---

#[human-interval](https://www.npmjs.com/package/human-interval)
> Human readable interval parser.

`human-interval` with 60 lines of code and some smart use of regexps provides a easy way to parser intervals in human readable form.

__Get it:__ `npm install --save human-interval`

__Sample usage:__

```js
const humanInterval = require('human-interval');

setTimeout(() => {
  // Do something crazy!
}, humanInterval('three minutes'));
```

```js
humanInterval('one minute');
humanInterval('1.5 minutes');
humanInterval('3 days and 4 hours');
humanInterval('3 days, 4 hours and 36 seconds');
```

__GIF FTW!__

![human-interval](/images/human-interval.gif)