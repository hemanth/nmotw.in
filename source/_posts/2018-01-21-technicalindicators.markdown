---
layout: post
title: "technicalindicators"
date: 2018-01-21 23:43:42 +0530
comments: true
categories: crypto
---

#[technicalindicators](https://www.npmjs.com/package/technicalindicators)
> Techincal Indicators!

Techincal Indicators: "Any class of metrics whose value is derived from generic price activity in a stock or asset."

With this module we would get around 20 indicators, 2 charts, 23 candle stick patterns!

__Get it:__ `npm install technicalindicators`

__Sample usage:__

```js
var twoDayBullishInput = {
  open: [23.25,15.36],
  high: [25.10,30.87],
  close: [21.44,27.89],
  low: [20.82,14.93],
}

var bullish = require('technicalindicators').bullish;

bullish(twoDayBullishInput) //true
```

__GIF FTW!__

![technicalindicators.gif](/images/technicalindicators/technicalindicators.gif)

