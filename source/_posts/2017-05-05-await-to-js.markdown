---
layout: post
title: "await-to-js"
date: 2017-05-05 03:00:13 +0000
comments: true
categories: ES7
---

#[await-to-js](https://www.npmjs.com/package/await-to-js)
> Async await wrapper for easy error handling!

Uber tiny module (10LOC) for making life easier while handling error while async-await.

This module is influenced by GoLang style of handling errors:

```
data, err := db.Query("SELECT ...")  
if err != nil { return err }  
```

We would basically covert the below code:

```js
const asyncTask = async () => {
  try {
    const answer = await Promise.resolve(42);
    // any async task.
  } catch(err) {
    // Handle error.
  }
  return answer;
}
```

to:

```js
const to = require("await-to-js").default;

const asyncTask = async () => {
  [ err, result ] = await to(Promise.resolve(42));
  if (!err) retrun result;
}

const answer = await asyncTask();
```

__Get it:__ `npm install --save await-to-js`

__GIF FTW!__

![await-to-js](/images/await-to-js/await-to-js.gif)

