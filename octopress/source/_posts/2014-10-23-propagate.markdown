---
layout: post
title: "propagate"
date: 2014-10-23 18:08:23 +0530
comments: true
categories: test, util
---

# [propagate](https://www.npmjs.org/package/propagate)
> Propagate events from one event emitter into another.

An other sweet and simple module, that helps to propagate events!

__Get it:__ `npm install propagate`

__Sample usage:__

```javascript
var EventEmitter = require('events').EventEmitter;
var propagate = require('propagate');

var evn1 = new EventEmitter();
var evn2 = new EventEmitter();

propagate(evn1,evn2);

evn2.on('event',function(msg) {
	console.log('Got a propagated event', msg);
});

evn1.emit('event', 'Yo!')
// Got a propagated event Yo!
```

__GIF FTW!__

![propagate](/images/propagate/propagate.gif)

Thanks to [Pedro Teixeira](http://metaduck.com/) for [propagate](https://www.npmjs.org/package/propagate).