---
layout: post
title: "fetch-mock"
date: 2019-04-21 11:45:27 +0530
comments: true
categories: util
---

#[fetch-mock](https://www.npmjs.com/package/fetch-mock)
> Mock HTTP requests with fetch.

`fetch-mock` allows mocking HTTP requests made using `fetch` or a library imitating its api, such as `node-fetch` or `fetch-ponyfill`, works across, browser and node.

__Get it:__ `npm install fetch-mock`

__Sample usage:__

```js
const fetchMock = require("fetch-mock");
fetchMock.mock('http://example.com', 200);
const res = await fetch('http://example.com');
console.log(res.ok); // true
```

__GIT FTW!__

![fetch-mock](/images/fetch-mock/fetch-mock.gif)

