---
layout: post
title: "glob-to-regexp"
date: 2019-04-14 00:11:35 +0530
comments: true
categories: util 
---

#[glob-to-regexp](https://www.npmjs.com/package/glob-to-regexp)
> `*-wildcard` style glob to R.E

`glob-to-regexp` helps us in converting *-wildcard style glob to RE, as in `"*.min.js"` to `/^.*\.min\.js$/`.

__Get it:__ `npm install glob-to-regexp`

__Sample usage:__

```js
const globToRegExp = require('glob-to-regexp');
```

```js
let re = globToRegExp("p*uck");
re.test("pot luck"); // true
re.test("pluck"); // true
re.test("puck"); // true
```

```js
re = globToRegExp("*.min.js");
re.test("http://example.com/jquery.min.js"); // true
re.test("http://example.com/jquery.min.js.map"); // false
```

```js
re = globToRegExp("*/www/*.js");
re.test("http://example.com/www/app.js"); // true
re.test("http://example.com/www/lib/factory-proxy-model-observer.js"); // true
```

```js
// Extended globs
re = globToRegExp("*/www/{*.js,*.html}", { extended: true });
re.test("http://example.com/www/app.js"); // true
re.test("http://example.com/www/index.html"); // true
```

__GIF FTW!__

![glob-to-regexp](/images/glob-to-regexp/glob-to-regexp.gif)