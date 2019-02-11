---
layout: post
title: "soted-object"
date: 2019-02-09 11:55:29 +0530
comments: true
categories: util 
---

#[sorted-object](https://www.npmjs.com/package/sorted-object)
> sort object by keys.

`sorted-object` is an uber tiny module that helps us sort an object by it's keys.

P.S: It got a `232,037` downloads last week ;)


__Get it:__ `npm install sorted-object`

__Sample usage:__

```js
const sortedObject = require('sorted-object')

sortedObject({b:1,c:2,a:3,0:0})
// => { '0': 0, a: 3, b: 1, c: 2 }
```

__GIF FTW!__

![sorted-object](/images/sorted-object/sorted-object.gif)
