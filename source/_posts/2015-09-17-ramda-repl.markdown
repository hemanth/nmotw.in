---
layout: post
title: "ramda-repl"
date: 2015-09-17 16:39:50 +0000
comments: true
categories: CLI functional 
---

# [ramda-repl](https://www.npmjs.com/package/ramda-repl) 
> [Ramda](http://ramdajs.com/) + [ramda-fantasy](https://www.npmjs.com/package/ramda-fantasy) REPL 

`ramda-repl` extends node REPL to bring in `Ramda` and `ramda-fantasy` so that you can use all of uber cool feature of ramda!

__Get it:__

```
$ npm install --save ramda-repl
```


__usage:__

```js
var ramdaRepl = require('ramda-repl');

ramdaRepl();
//=> Will start a REPL
```


## CLI

```sh
$ npm install --global ramda-repl
```

$ ramda-repl

__Will start a REPL as below with `R` as well as current context is extended with ramda__

```
Welcome to Ramda REPL!

λ > typeof R 
'object'

λ > typeof map
'function'

λ > typeof zipWith
'function'

```

## GIF FTW

![ramda-repl](/images/ramda-repl/ramda-repl.gif)

## License

MIT © [Hemanth.HM](http://h3manth.com)