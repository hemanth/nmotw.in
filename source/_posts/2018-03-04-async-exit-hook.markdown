---
layout: post
title: "async-exit-hook"
date: 2018-03-04 11:56:54 +0530
comments: true
categories: util
---

#[async-exit-hook](https://www.npmjs.com/package/async-exit-hook)
> Run some code when the process exits.

`async-exit-hook` is a fork from `exit-hook` which can catch:

* process SIGINT, SIGTERM and SIGHUP, SIGBREAK signals
* process beforeExit and exit events
* PM2's exit.

As `process.on('exit')` event doesn't catch all the ways a process can exit.

__Get it:__ `npm install async-exit-hook`

__Sample usage:__

```js
exitHook(() => {
    console.log('exiting');
});

exitHook(callback => {
    setTimeout(() => {
        console.log('exiting');
        callback();
    }, 1000);
});
```

__GIF FTW__

![async-exit-hook](/images/async-exit-hook/async-exit-hook.gif)



