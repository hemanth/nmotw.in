---
layout: post
title: "why-is-node-running"
date: 2016-02-11 15:04:17 +0000
comments: true
categories: debug
---

#[why-is-node-running](https://www.npmjs.com/package/why-is-node-running)
> Node is running but you don't know why? why-is-node-running is here to help you.

This is a cheeky module that plays with `process.binding` of node, specifically with `process.binding('contextify').ContextifyScript;` the core of this library is from node's [source](https://github.com/nodejs/node/blob/88307974e60346bc98c4e9f70a2b6918ccb6844f/src/node.js).

__GET IT:__ `npm install --save why-is-node-running`

__Sample usage:__

```js
var log = require('why-is-node-running'); // should be your first require 
var net = require('net');
 
function createServer () {
  var server = net.createServer();
  setInterval(function () {}, 1000);
  server.listen(0);
}
 
createServer();
createServer();
 
setTimeout(function () {
  log() // logs out active handles that are keeping node running 
}, 100);
```

When executed in `/tmp` you see an output like:


```sh
There are 4 known handle(s) keeping the process running and 0 unknown
Known handles:

# Timer
/private/tmp/l:6  - setInterval(function () {}, 1000);
/private/tmp/l:10 - createServer();

# TCP
/private/tmp/l:7  - server.listen(0);
/private/tmp/l:10 - createServer();

# TCP
/private/tmp/l:7  - server.listen(0);
/private/tmp/l:11 - createServer();

# Timer
/private/tmp/l:13 - setTimeout(function () {
```

__GIF FTW!__

![why-is-node-running](https://nmotw.in/images/why-is-node-running/why-is-node-running.gif)


