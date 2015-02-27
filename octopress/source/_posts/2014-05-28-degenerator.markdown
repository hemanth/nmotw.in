---
layout: post
title: "degenerator"
date: 2014-05-29 20:22:17 +0530
comments: true
categories: generators es6
ogimg: http://nmotw.in/images/degenerator/degenerator.gif
---

Turns sync functions into ES6's async generator functions with [Nathan Rajlich's](http://n8.io/) (A.K.A TooTallNate) [degenerator](https://www.npmjs.org/package/degenerator)


Get it: `$ npm install degenerator`

__Example Usage:__


Say we have few sync function like:

```javascript
function foo () {
  return baz();
}

function bar () {
  return foo(baz);
}

function baz () {
  return bar();
}
```

Some degenerator magic!

```javascript
var degenerator = require('degenerator')
var js = fs.readFileSync(sourceName, 'utf8');
var compiled = (js, ['foo','bar','baz']);
```

The complied source would be:

```javascript
function* foo() {
    return yield baz();
}
function* bar() {
    return yield foo(baz);
}
function* baz() {
    return yield bar();
}
```

__GIF FTW!__

![degnerator](/images/degenerator/degenerator.gif)
