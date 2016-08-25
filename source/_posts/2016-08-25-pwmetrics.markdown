---
layout: post
title: "pwmetrics"
date: 2016-08-25 13:33:31 +0000
comments: true
categories: performance util
---

# [pwmetrics](https://www.npmjs.com/package/pwmetrics)

> Progressive web metrics at your fingertipz. 💅


`pwmetrics` CLI tool and lib to gather performance metrics via [Lighthouse](https://github.com/GoogleChrome/lighthouse/).

P.S: This module is _IN BETA_, so you must be ready for anything 😉


__GET IT:__ `npm install --global pwmetrics` or `npm install --save pwmetrics`


__Sample CLI usage:__

```sh
# run Chrome with port 9222 open
chrome  --remote-debugging-port=9222 --no-first-run --user-data-dir=$(mktemp -d -t pwm.XXXXX)
```

```sh
# run pwmetrics with your url
pwmetrics https://jsfeatures.in
```


```sh
$ pwmetrics --json https://jsfeatures.in
{
  "timings": [
    {
      "name": "First Contentful Paint",
      "value": 1875.337
    },
    {
      "name": "First Meaningful Paint",
      "value": 1970.7
    },
    {
      "name": "Median Visual Completion",
      "value": 1997
    },
    {
      "name": "First Visual Change",
      "value": 1917
    },
    {
      "name": "Visually Complete 100%",
      "value": 2004
    },
    {
      "name": "Time to Interactive",
      "value": -1
    },
    {
      "name": "Visually Complete 85%"
    },
    {
      "name": "Navigation Start",
      "value": 0
    }
  ],
  "timestamps": [
    303915241.28
  ]
}
```

__API:__


```js
const PWMetrics = require('pwmetrics');

new PWMetrics('https://jsfeatures.in', opts); // opts => {data:fileName} for now.
```

__GIF FTW!:__

![pwmetrics](/images/pwmetrics/pwmetrics.gif)
