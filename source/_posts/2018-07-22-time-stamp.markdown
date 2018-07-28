---
layout: post
title: "time-stamp"
date: 2018-07-22 15:12:10 +0730
comments: true
categories: util time 
---

#[time-stamp]()
>Get a formatted timestamp.

How many times have you created time stamp in your code base? 

`time-stamp` makes it easy to create them, this module revovles around the R.E -> `/(?=(YYYY|YY|MM|DD|HH|mm|ss|ms))\1([:\/]*)/;`

__Supported formats:__

```
YYYY: full year (ex: 2018)
MM: month (ex: 04)
DD: day (ex: 01)
HH: hours (ex: 12)
mm: minutes (ex: 59)
ss: seconds (ex: 09)
ms: milliseconds (ex: 532)
```

__Sample usage:__


```js

const timeStamp = require("time-stamp");

timestamp();
//=> 2018-07-23

timestamp('YYYYMMDD');
//=> 20180723

timestamp('YYYYMMDD:ss');
//=> 20180723:10

timestamp('YYYY/MM/DD:mm:ss');
//=> 2018/07/23:30:10

timestamp('YYYY:MM:DD');
//=> 2018:07:23

timestamp('[YYYY:MM:DD]');
//=> [2018:07:23]

timestamp('YYYY/MM/DD');
//=> 2018/07/23

timestamp('YYYY:MM');
//=> 2018:07

timestamp('YYYY');
//=> 2018

timestamp('MM');
//=> 07

timestamp('DD');
//=> 23

timestamp('HH');
//=> 21

timestamp('mm');
//=> 30

timestamp('ss');
//=> 10

timestamp('ms');
//=> 365

```

__GIF FTW__

![time-stamp](/images/time-stamp/time-stamp.gif)