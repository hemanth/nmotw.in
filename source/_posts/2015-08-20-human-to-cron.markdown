---
layout: post
title: "human-to-cron"
date: 2015-08-20 12:39:33 +0000
comments: true
categories: util cli
---

#[human-to-cron](https://www.npmjs.com/package/human-to-cron)
> Converts human readable expression to a cron string!

If you can interpert `0 */1 * * *` as `each minute` then this module is not for you ;) 

`human-to-cron` parsers the human readable expressions with the help of ES6 generators converts it into a [cron](https://en.wikipedia.org/wiki/Cron
) string.

__Get it:__ `npm install --save human-to-cron`

__Sample usage:__

```js
var humanToCron = require('human-to-cron');

humanToCron('once each minute') // => 0 */1 * * * *
humanToCron('each 2 minutes') // => * */2 * * * *
humanToCron('each second') // => */1 * * * * *
humanToCron('once each hour') // => 0 0 */1 * * *
humanToCron('once each day') // => 0 0 0 */1 * *
humanToCron('once each month') // => 0 0 0 0 */1 *
humanToCron('once each 5 months') // => 0 0 0 0 */5 *
humanToCron('midnight') // => 0 0 0 * * *
humanToCron('midnight each 2 minutes') // => 0 */2 0 * * *
humanToCron('once tuesday each 10 minutes') // => 0 */10 * 1 * *
humanToCron('friday 15:44') // => 0 44 15 4 * *
humanToCron('august friday 15:44') // => 0 44 15 4 7 *
```

__GIF FTW!__

![human-to-cron](/images/human-to-cron/human-to-cron.gif)

Thanks to [Andrius Skerla](https://github.com/rainder) for this cheeky module! 