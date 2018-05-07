---
layout: post
title: "global-cache"
date: 2018-05-05 11:45:30 +0530
comments: true
categories: util 
---

#[global-cache](https://www.npmjs.com/package/global-cache)
> Use global object as a share singleton.


From the 🐴's mouth -> Sometimes you have to do horrible things, like use the global object to share a singleton. Abstract that away, with this!

`global-cache` attaches a cache to the global object. It attempts to make it as undiscoverable as possible:

* uses Symbols if available

* if not, uses a string key that is not a valid identifier, so as not to show up in dot-notation browser autocomplete

* makes it non-enumerable if property descriptors are supported

* keys are required to be strings or symbols.

__Get it:__ `npm install global-cache`

__Sample usage:__

```js
let value = {}, key='key';
const cache = require('global-cache');

[cache.get(key), cache.has(key)]; //[ undefined, false ]

cache.set(key,value); //true

[cache.get(key), cache.has(key)]; //[ {}, true ]

cache.delete(key); // true

[cache.get(key), cache.has(key)]; // [ undefined, false ]

cache
/*
{ clear: [Function: clear],
  delete: [Function: deleteKey],
  get: [Function: get],
  has: [Function: has],
  set: [Function: set],
  setIfMissingThenGet: [Function: setIfMissingThenGet] }
*/
```

__GIT FTW!__

![global-cache.gif](/images/global-cache/global-cache.gif)

