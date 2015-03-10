---
layout: post
title: "dompurify"
date: 2015-03-05 13:17:23 +0000
comments: true
categories: dom
---

# [dompurify](https://www.npmjs.com/package/dompurify)
> Super-fast, uber-tolerant XSS sanitizer for HTML, MathML and SVG!


DOMPurify sanitizes HTML and prevents XSS attacks. 

|dirty HTML |  => |DOMPurify.sanitize |  => | Clean and safe HTML |


The faster your browser, the faster DOMPurify will be ;)


__Install it:__  ```npm install --save dompurify```


__Sample usage:__

```js

var DOMpurify = require('dompurify);

DOMPurify.sanitize('<img src=x onerror=alert(1)//>'); // becomes <img src="x"> 

DOMPurify.sanitize('<svg><g/onload=alert(2)//<p>'); // becomes <svg><g></g></svg>

```

It's configurable: `var config = { ALLOWED_TAGS: ['p', '#text'], KEEP_CONTENT: false };` and `DOMPurify.sanitize(str, config)`

We can also use `hooks`:

* beforeSantitizeElements

* afterSantitizeElements

* beforeSantitizeAttributes

* afterSantitizeAttributes


```js
DOMPurify.addHook('beforeSantitizeElements', function(currentNode, config) {
    // Play with currentNode.
    return currentNode;
});
```

__GIF FTW!__

![dompurify](/images/dompurify/dompurify.gif)
