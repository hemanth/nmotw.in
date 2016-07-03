---
layout: post
title: "node-nightly"
date: 2016-06-30 12:31:14 +0000
comments: true
categories: node cli
---

#[node-nightly](https://www.npmjs.com/package/node-nightly)
> node-nightly at your finger tips!

`node-nightly` as the name says it's the nightly version of `node`, basically:

* Check if nightly version of node is available if not install it. (For the first time.)

* If there is a new version available will notify the user saying there is a newer version available and can update using `node-nightly --update`

__Get it__ : `npm install -g node-nightly` # Preferred global


__Sample usage:__

```js
$ node-nightly --inspect --debug-brk index.js
Debugger listening on port 9229.
To start debugging, open the following URL in Chrome:
    chrome-devtools://devtools/remote/serve_file/@521e5b7e2b7cc66b4006a8a54cb9c4e57494a5ef/inspector.html?experiments=true&v8only=true&ws=localhost:9229/node
Debugger attached.
Waiting for the debugger to disconnect...
```

__GIF FTW!__

![node-nightly](/images/node-nightly/node-nightly.gif)
