---
layout: post
title: "safe-json-parse"
date: 2015-01-08 22:26:50 +0530
comments: true
categories: json util
---

# [safe-json-parse](https://www.npmjs.com/package/safe-json-parse)
> Parse JSON safely without throwing.

Sweet, simple and effictive module for parsing JSON safely :)

__Get it:__ `npm install safe-json-parse --save`

__Sample usage:__

With callback:

```js
> var sf = require('safe-json-parse');

> sf("{}", function (err, json) {console.log(err,json);});
null {}

> sf("meow", function (err, json) {console.log(err,json);});
[SyntaxError: Unexpected token m] undefined

```

As Tuples:

```js
> var sf = require('safe-json-parse/tuple');
> sf({})
[ [SyntaxError: Unexpected token o], undefined ]
> sf("{}")
[ null, {} ]
```

__GIF FTW!__

![safe-json-parse](/images/safe-json-parse/safe-json-parse.gif )

Thanks to [Raynos](https://twitter.com/raynos) for helping us with safely parsing JSONs ;)
