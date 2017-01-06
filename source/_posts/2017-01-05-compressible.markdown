---
layout: post
title: "compressible"
date: 2017-01-05 14:32:05 +0000
comments: true
categories: content-type mime gzip compress
---

#[compressible](https://www.npmjs.com/package/compressible)
> Compressible `Content-Type/mime` checking

Sweet and simple module that Checks if the given `Content-Type` is compressible. 

The type argument is expected to be a value `MIME` type or `Content-Type` string, though no validation is performed.

The `MIME` is looked up in the `mime-db` and supports:

* text/*
* */*+json
* */*+text
* */*+xml

__Get it:__ `npm install --save compressible` 


__Sample usage:__


```js
const compressible = require('compressible');

compressible('image/png'); // false

compressible('image/pn'); // undefined

compressible('text/html'); // true
```

__GIF FTW!__

![compressible](/images/compressible/compressible.gif)

