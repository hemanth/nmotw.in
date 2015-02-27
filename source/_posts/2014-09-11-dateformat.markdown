---
layout: post
title: "dateformat"
date: 2014-09-11 18:25:04 +0530
comments: true
categories: util
ogimg: http://nmotw.in/images/dateformat/dateformat.gif
---

# dateformat

>Steven Levithan's excellent [dateFormat()][dateformat] function.


## Installation

```bash
$ npm install dateformat
```

## Usage

```js
    var dateFormat = require('dateformat');
    var now = new Date();

    dateFormat(now, "dddd, mmmm dS, yyyy, h:MM:ss TT");

    dateFormat(now, "isoDateTime");

    dateFormat.masks.foodTime = 'HH:MM! "Time to eat!"';

    dateFormat(now, "foodTime");

    dateFormat("Feb 1 1988", "fullDate");

```

__GIF FTW:__

![](/images/dateformat/dateformat.gif)


Thanks to the author [Felix Geisendörfer](https://twitter.com/felixge) for a sweet date formatter! :)

[dateformat]: http://blog.stevenlevithan.com/archives/date-time-format
[stevenlevithan]: http://stevenlevithan.com/
