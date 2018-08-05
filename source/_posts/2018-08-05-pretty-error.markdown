---
layout: post
title: "pretty-error"
date: 2018-08-05 13:37:39 +0530
comments: true
categories: human util
---

#[pretty-errror](https://www.npmjs.com/package/pretty-error)
>errors with less clutter

`pretty-error` turns error objects into something similar to an html document, and then uses `RenderKid` to render the document using simple html/css-like commands.

__Get it:__ `npm install pretty-error`

__Sample usage:__

```js
const PrettyError = require('pretty-error');
const pe = new PrettyError();
 
const renderedError = pe.render(new Error('Some error message'));
console.log(renderedError);
```

```js
try {
   doSomethingThatThrowsAnError();
} catch (error) {
   console.log(pe.render(error));
}
```

__GIF FTW!__

![pretty-error](/images/pretty-error/pretty-error.gif)

