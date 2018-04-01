---
layout: post
title: "april-fools"
date: 2018-04-01 00:07:51 +0000
comments: true
categories: fun
---

[april-fools](https://www.npmjs.com/package/april-fools)
> Randomly fool with an `Error` on April 1st.

⚠️ This is a foolproof way to lose friends and alienate people. Will likely get you fired!

Few lines of code to have fun on April fools day:

```
'use strict'

const date = new Date()

if (date.getMonth() === 3 && date.getDate() === 1 && Math.floor(Math.random() * 6) + 1 === 1) {
  const message = require('sentencer').make("Unexpected {{ noun }} with {{ an_adjective }} {{ noun }}")

  throw new Error(message)
}
```

Related module -> [sentencer](http://nmotw.in/sentencer/).

__Sample usage:__

```js
require('april-fools'); // That's it! And it would randomly throw an error like below.

Error: Unexpected lunch with a brindle ravioli
    at Object.<anonymous> (/private/tmp/node_modules/april-fools/index.js:8:9)
    at Module._compile (module.js:652:30)
    at Object.Module._extensions..js (module.js:663:10)
    at Module.load (module.js:565:32)
    at tryModuleLoad (module.js:505:12)
    at Function.Module._load (module.js:497:3)
    at Module.require (module.js:596:17)
    at require (internal/module.js:11:18)
```

__GIF FTW__

![april-fools](/images/april-fools/april-fools.gif)
