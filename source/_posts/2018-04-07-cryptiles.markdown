---
layout: post
title: "cryptiles"
date: 2018-04-07 16:56:08 +0530
comments: true
categories: util
---

#[cryptiles](https://npmjs.com/package/cryptiles)
> General purpose crypto utilities.

`cryptiles` provides util methods for creating cryptographically strong pseudo-random data with the below methods:

* fixedTimeComparison
* randomBits
* randomDigits
* randomString

__Get it:__ `npm install cryptiles`

__Sample usage:__

```js
const cryptiles = require("cryptiles");
[
cryptiles.fixedTimeComparison('abcd','abcd'),
cryptiles.randomBits(5),
cryptiles.randomDigits(5),
cryptiles.randomString(5)
]

/* ^
[
  true,
  Uint8Array <66>,
  "42115",
  "jsmx9"
]
*/
```

__GIF FTW!__

![cryptiles](/images/cryptiles/cryptiles.gif)

