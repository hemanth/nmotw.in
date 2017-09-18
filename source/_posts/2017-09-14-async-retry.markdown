---
layout: post
title: "async-retry"
date: 2017-09-14 22:50:23 +0530
comments: true
categories: async 
---

#[async-retry](https://www.npmjs.com/package/async-retry)
> Retrying made simple, easy, async.

`async-retry` is a promisified version of [retry](https://www.npmjs.com/package/retry) which makes things easier with the `async-await` syntax.

__Get it:__ `npm install async-retry`

__Sample usage:__


```js
// Packages 
const retry = require('async-retry')
const fetch = require('node-fetch')
 
await retry(async bail => {
  // if anything throws, we retry 
  const res = await fetch('https://google.com')
 
  if (403 === res.status) {
    // don't retry upon 403 
    bail(new Error('Unauthorized'))
    return
  }
 
  const data = await res.text()
  return data.substr(0, 500)
}, {
  retries: 500
})
```

__Method signature:__

```
retry(retrier : Function, opts : Object) => Promise
```

__GIF FTW!__

![async-retry](/images/async-retry/async-retry.gif)
