---
layout: post
title: "instapromise"
date: 2015-10-08 12:15:41 +0000
comments: true
categories: promise, util
---

#[instapromise](https://www.npmjs.com/package/instapromise)
> Promisify with `.promise`

`instapromise` lets you promisify node-style asynchronous functions by putting a `.promise` after them or after the object for methods.

It's a part of [exponent](http://exponentjs.com/) and this module is influenced from [fibrous](https://www.npmjs.com/package/fibrous).

When one of the maintainers of `instapromise` was questioned about why the code was in coffeescript :

There’s basically two reasons for that:

* It’s based on some of the work the people who made fibrous did and they wrote their stuff in coffeescript

* I used to write a bunch of coffeescript before babel made it reasonable to write ES7+ stuff

* I wrote it back then, its pretty stable now.

* I haven’t made any changes to it in months so I don’t think it should be necessary to modify the source too much.

* Also I do like the way that its commented fairly well.

__Get it:__ ```npm install --save instapromise```

__Usage:__

```js
require(‘instapromise’);
let val = await someObject.promise.someMethodThatTakesANodeStyleCallback(‘but not anymore’);
```
  
Basically, `instapromise` is one of it's kind a module that is cheeky, tiny and takes a diffrenet apporach on promisifying async functions,
you need to just `require('instapromise')` and then you could just use a `.promise`!

```js
require('instapromise');
var fs = require('fs');
var p = fs.promise.readFile('/tmp/hello', 'utf8');
p.then(console.log);
```

P.S: The original function is available as a property on the promise-generating function `.___instapromiseOriginalFunction___`

__GIF FTW!__

![instapromise](/images/instapromise/instapromise.gif)

Thanks to [James Ide](https://twitter.com/JI) and [Charlie Cheever](https://twitter.com/ccheever) for instapromise! 

  