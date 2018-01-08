---
layout: post
title: "circular-json"
date: 2018-01-07 11:38:12 +0530
comments: true
categories: util
---

#[circular-json](https://www.npmjs.com/package/circular-json)
> Handle circular JSON references with ease!

You would have come acorss `TypeError: Converting circular structure to JSON` if you have been handling JSONs for a while now, `circular-json` serializes and deserializes otherwise valid JSON objects containing circular references into and from a specialized JSON format.

__Get it:__ `npm install circular-json`

__Sample usage:__

```js
'use strict';

const
  CircularJSON = require('circular-json'),
  obj = { foo: 'bar' },
  str
;

obj.self = obj;
const str = CircularJSON.stringify(obj);

// "{\"foo\":\"bar\",\"self\":\"~\"}"

/*
JSON.stringify(obj); would have resulted in:
TypeError: Converting circular structure to JSON
*/
```

__GIF FTW!__

![circular-json](/images/circular-json/circular-json.gif)

