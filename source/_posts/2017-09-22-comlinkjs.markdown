---
layout: post
title: "comlinkjs"
date: 2017-09-22 12:02:46 +0530
comments: true
categories: util 
---

#[comlinkjs](https://www.npmjs.com/package/comlinkjs)
> A tiny RPC library for windows, iframes, WebWorkers and ServiceWorkers.

`comlinkjs` has the below interface, makes use of `MessageChannel` helps you to work on objects from another JavaScript realm (like a Worker or an iframe) as if it was a local object. Just use await whenever the remote value is involed.

```js
interface Endpoint {
    postMessage(message: any, transfer?: any[]): void;
    addEventListener(type: string, listener: EventListenerOrEventListenerObject, options?: {}): void;
    removeEventListener(type: string, listener: EventListenerOrEventListenerObject, options?: {}): void;
}
declare type Proxy = Function;

declare const Comlink: {
    proxy: (endpoint: Window | Endpoint) => Function;
    proxyValue: (obj: {}) => {};
    expose: (rootObj: Object | Function, endpoint: Window | Endpoint) => void;
};
```

__Get it:__ `npm install comlinkjs`

__Sample usage:__


```js
// On the site:
  const worker = new Worker('worker.js');
  // WebWorkers use `postMessage` and therefore work with Comlink.
  const api = Comlink.proxy(worker);
 
  (async function init() {
    // Note the usage of `await`:
    const app = await new api.App();
    console.log(`Counter: ${await app.count}`);
    await app.inc();
    console.log(`Counter: ${await app.count}`);
  }());
```

```js
// In the worker
class App {
  constructor() {
    this._counter = 0;
  }
 
  get count() {
    return this._counter;
  }
 
  inc() {
    this._counter++;
  }
}
 
Comlink.expose({App}, self);
```

__GIF FTW!__

![comlinkjs](/images/comlinkjs/comlinkjs.gif)

