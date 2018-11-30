---
layout: post
title: "progress-estimator"
date: 2018-11-30 08:54:21 +0530
comments: true
categories: util promise
---

#[progress-estimator]()
> Progress bar and estimation for Promise compilation.

`progress-estimator` logs a progress bar and estimation for how long a Promise will take to complete. 

It tracks previous durations in order to provide more accurate estimates over time!

__Get it:__ `npm install progress-estimator`

__Sample usage:__

```js
const createLogger = require('progress-estimator');

// All configuration keys are optional, but it's recommended to specify a storage location.
// Learn more about configuration options below.
const logger = createLogger({
  storagePath: join(__dirname, '.progress-estimator'),
});

async function run() {
  await logger(promiseOne, "This is a promise");
  await logger(
    promiseTwo,
    "This is another promise. I think it will take about 1 second",
    {
      estimate: 1000
    }
  );
}
```

__GIF FTW!__

![progress-estimator](/images/progress-estimator/progress-estimator.gif)


