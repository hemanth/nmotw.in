---
layout: post
title: "objectmap"
date: 2015-02-05 19:33:17 +0530
comments: true
categories: es6 util 
---

#[mapobject](https://www.npmjs.com/package/mapobject)
> Use a ES6 map, like an object.

This module is one of those rare hidden gems in npm, it's already a year old, it makes uses of ES6 reflect API with proxy to make give us a convience method so that maps can be used like an Object.

What other advantages apart from syntax sugar?

* Iterate it like a regular object with `(for in)` without worrying about `hasOwnProperty` checks.

* Iterate it `(for of)` you will get arrays of length 2 of both keys and values.



__Install it:__ `npm install --save objectmap`

__Sample usage:__

```js

var oMap = require('objectmap');

var map = oMap();

map.answer = 42; // Same as `map.set('answer',42);`

map.answer; // Same as `map.get('abc');`

delete map.abc; // Same as `map.delete('abc');`

```

Caveat: `map[3]` implies `map.set('3')` not `map.set(3)`


__GIF FTW!__

![](/images/objectmap/objectmap.gif)


Thanks to [Calvin](http://calvinmetcalf.com) for this useful util :)







