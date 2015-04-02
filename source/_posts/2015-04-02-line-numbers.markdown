---
layout: post
title: "line-numbers"
date: 2015-04-02 11:40:30 +0000
comments: true
categories: util
---

#[line-numbers](https://www.npmjs.com/package/line-numbers)
> Add line numbers to a string.

A humble module that will add line number to a given string! Mostly useful for text editor and displaying some code snippet.

__Install it:__ `$ npm install --save line-numbers`

__Simple usage:__

```js

var lns = require('line-numbers');

code = `function meow(cb) { 
  if(!cb) throw new Error("CB is a must!");
  cb("meow");
}`

console.log( lns(code) );

/*
Would log:

 1 | function meow(cb) { 
 2 |   if(!cb) throw new Error("CB is a must!");
 3 |   cb("meow");
 4 | }
*/
```

P.S: You can also pass in options like: `before`, `number`, `width`, `after` and `line` (They are self explanatory?)


__GIF FTW!__

![line-numbers](/images/line-numbers/line-numbers.gif)


Thanks to Simon Lydell for `line-numbers`.
