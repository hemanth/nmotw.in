---
layout: post
title: "proxymise"
date: 2018-07-15 15:52:27 +0530
comments: true
categories: util promise  
---

#[proxymise](https://www.npmjs.com/package/proxymise)
> Chainable Promise Proxy.

`proxymise` makes cheeky use of [Proxy](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy) API and provides a high dose of syntax sugar in chaining promises.

__Get it:__ `npm install proxymise`

__Sample usage:__


```
const proxymise = require('proxymise');
```

```
// Instead of thens
foo.then(value => value.bar())
  .then(value => value.baz())
  .then(value => value.qux)
  .then(value => console.log(value));
```

```
// Instead of awaits
const value1 = await foo;
const value2 = await value1.bar();
const value3 = await value2.baz();
const value4 = await value3.qux;
console.log(value4);
```

```
// Use proxymise
const value = await proxymise(foo).bar().baz().qux;
console.log(value);
```

__GIF FTW__

![proxymise](/images/proxymise/proxymise.gif)
