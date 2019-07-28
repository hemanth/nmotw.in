---
layout: post
title: "responselike"
date: 2019-07-28 14:12:19 +0530
comments: true
categories: util testing
---

#[responselike](https://www.npmjs.com/package/responselike)
> response-like object for mocking HTTP response stream.

`responselike` returns a streamable response object similar to a HTTP response stream. Useful for formatting cached responses so they can be consumed by code expecting a real response.

__Get it:__ `npm install responselike`

__Sample usage:__

```js
const Response = require('responselike');
 
const response = new Response(200, { foo: 'bar' }, Buffer.from('Hi!'), 'https://example.com');
 
response.statusCode;
// 200
response.headers;
// { foo: 'bar' }
response.body;
// <Buffer 48 69 21>
response.url;
// 'https://example.com'
 
response.pipe(process.stdout);
// Hi!
```

__GIF FTW!__

![responselike](/images/responselike/responselike.gif)



