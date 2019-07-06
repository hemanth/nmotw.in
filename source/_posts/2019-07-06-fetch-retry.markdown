---
layout: post
title: "fetch-retry"
date: 2019-07-06 14:23:46 +0530
comments: true
categories: util
---

#[fetch-retry](https://www.npmjs.com/package/fetch-retry)
> Adds retry functionality to the Fetch API.

`fetch-retry` in about 88 lines of code provides an extension to the `fetch` API to accept `retries`, `retryDelay`, and `retryOn` on the options object, when omitted will default to 3 retries, a 1000ms retry delay, and to retry only on network errors.

__Get it:__ `npm install fetch-retry`

__Smaple usages:__

```js
const  fetch = require('fetch-retry');
```

```js
fetch(url, {
    retries: 3,
    retryDelay: 1000
  })
  .then(function(response) {
    return response.json();
  })
  .then(function(json) {
    // do something with the result
    console.log(json);
  });
```

```js
// Retry on 503
fetch(url, {
    retryOn: [503]
  })
  .then(function(response) {
    return response.json();
  })
  .then(function(json) {
    // do something with the result
    console.log(json);
  });
```

```js
// Custorm retry
fetch(url, {
    retryOn: function(attempt, error, response) {
      // retry on any network error, or 4xx or 5xx status codes
      if (error !== null || response.status >= 400) {
        console.log(`retrying, attempt number ${attempt + 1}`);
        return true;
      }
    })
    .then(function(response) {
      return response.json();
    }).then(function(json) {
      // do something with the result
      console.log(json);
    });
}
```

__GIF FTW!__

![fetch-retry](/images/fetch-retry/fetch-retry.gif)
