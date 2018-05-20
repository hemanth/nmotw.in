---
layout: post
title: "signal-exit"
date: 2018-05-20 20:33:02 +0530
comments: true
categories: util cli
---

#[signal-exit](https://www.npmjs.com/package/signal-exit)
> Fire an event no matter how a process exits.

`signal-exit` fires an event no matter how a process exits:

* reaching the end of execution.
* explicitly having `process.exit(code)` called.
* having `process.kill(pid, sig)` called.
* receiving a fatal signal from outside the process


__Get it:__ `npm install signal-exit`

__Sample code:__

```js
var onExit = require('signal-exit')
 
onExit(function (code, signal) {
  console.log('process exited!', code, signal)
})
```

__GIF FTW!__

![signal-exit](/images/signal-exit/signal-exit.gif)
