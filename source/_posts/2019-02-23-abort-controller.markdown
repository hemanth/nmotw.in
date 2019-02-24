---
layout: post
title: "abort-controller"
date: 2019-02-23 11:10:52 +0530
comments: true
categories: util DOM
---

#[abort-controller](https://www.npmjs.com/package/abort-controller)
> An implementation of WHATWG AbortController interface.

The AbortController interface allows us to abort one or more DOM requests as per the need.

From the [sepc](https://dom.spec.whatwg.org/#interface-abortcontroller):

The `AbortController()` constructor, when invoked, must run these steps:

* Let signal be a `new AbortSignal` object.

* Let controller be a `new AbortController` object whose signal is signal.

* Return controller.

The `signal` attribute’s getter, when invoked, must return the context object’s signal.

The `abort()` method, when invoked, must signal abort on the context object’s signal.

__Get it:__ `npm install abort-controller`

__Usage:__

```js
import AbortController from "abort-controller";
// or
const AbortController = require("abort-controller");

// or UMD version defines a global variable:
const AbortController = window.AbortControllerShim;
```


```js
import AbortController from "abort-controller";

const controller = new AbortController();
const signal = controller.signal;

signal.addEventListener("abort", () => {
    console.log("aborted!");
})

controller.abort();
```

__GIF FTW!__

![abort-controller](/images/abort-controller/abort-controller.gif)
