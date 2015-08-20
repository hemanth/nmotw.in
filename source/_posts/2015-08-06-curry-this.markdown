---
layout: post
title: "curry-this"
date: 2015-08-06 15:16:13 +0000
comments: true
categories: util ES7
---

#Curry-this

`Curry-this` makes creating curryied function simple and expresive by invoking `curry` with the [function bind syntax `::`](https://github.com/zenparsing/es-function-bind).
Apart from the expresive way of creating a curried function, the main feature are placeholders.
A placeholder (`_`) is a [`Symbol`](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Symbol) which allows to curry specific arguments of a function.

**Install it:** `npm install --save curry-this`

## Basic usage

```js
const {curry, _} = require('curry-this')();


// Got a simple function?

const plus = (
    (a, b, c) => a + b + c
)::curry();

plus(1, 2, 3);  //» 6
plus(1)(2, 3);  //» 6
plus(1, 2)(3);  //» 6
plus(1)(2)(3);  //» 6
```

## Placeholders

```js
// Got a monster function?

const {open} = require('fs');
const newScript = open::curry(_, 'w', 0755, _);

newScript('do-wonders.sh', (error, file) => {
  // The `file` is ready.
});
```

You can try this with `babel-node`. Make sure that you use the `--stage=0` option.

__GIF FTW!__

![curry-this](/images/curry-this/curry-this.gif)


Thanks to [Christoph Hermann](http://stoeffel.github.io/) and [tomekwi](https://github.com/tomekwi) for making cury more fun!