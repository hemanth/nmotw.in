---
layout: post
title: "require-times"
date: 2015-04-09 14:40:22 +0000
comments: true
categories: debug
---

#[require-times](http://npm.im/require-times)
> Find out how long require calls take in your program.

This is cheeky module from [Max Ogden](http://maxogden.com/) tap into `require.extensions['.js']` and lets you know the time consumed by
the require calls in your code.

__Install it:__ `npm install require-times`


__Usage:__

```js
var rt = require('require-times');
rt.start();

// hundreds on require statments ;)

rt.end(); // Will spit the time consumed to stdout.
```

__Example:__

```js
var rt = require('require-times')();

rt.start();

require('require-times'); // Dog fooding ;)

rt.end();

// Output => total: 9647ms
```

__GIF FTW!__

![require-times](/images/require-times/require-times.gif)
