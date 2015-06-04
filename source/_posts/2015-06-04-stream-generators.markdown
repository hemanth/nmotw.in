---
layout: post
title: "stream-generators"
date: 2015-06-04 20:27:12 +0000
comments: true
categories: ES6 streams 
---

[stream-generators](https://www.npmjs.com/package/stream-generators)
> Pipe ES6 Generators through Node.js streams.

This is a cheeky module authored by [@mimetent](https://twitter.com/mimetnet) which takes in a ES6 generator function and returns a readable stream!


__Install it:__ `npm install --save stream-geerators`



__Sample usage:__


```js
var streamify = require('stream-generators'),
    os = require('os')
    gen = function*() {
        yield 'Hello ';
        yield 'ES6 ';
        yield 'Stream gen';
        yield os.EOL;
    };
;

streamify(gen).pipe(process.stdout);
```

This would output: `Hello ES6 Stream gen`


__GIF FTW!__

![stream-generators](/images/stream-generators/stream-generators.gif)
