---
layout: post
title: "error-stack-parser"
date: 2018-07-01 20:42:55 +0530
comments: true
categories: util
---

#[error-stack-parser](https://npm.im/error-stack-parser)
> Simple, cross-browser Error parser.

`error-stack-parser` library parses and extracts function names, URLs, line numbers, and column numbers from the given Error's stack as an Array of StackFrames.

__Get it:__ `npm install error-stack-parser`

__Sample usage:__

```js

const ErrorStackParser = rquire("error-stack-parser);

ErrorStackParser.parse(new Error('BOOM'));

/*
=> [
        StackFrame({functionName: 'foo', args: [], fileName: 'path/to/file.js', lineNumber: 35, columnNumber: 79, isNative: false, isEval: false}),
        StackFrame({functionName: 'Bar', fileName: 'https://cdn.somewherefast.com/utils.min.js', lineNumber: 1, columnNumber: 832, isNative: false, isEval: false, isConstructor: true}),
        StackFrame(... and so on ...)
   ]
*/

Object.keys(ErrorStackParer);

/*
[ 'parse',
  'extractLocation',
  'parseV8OrIE',
  'parseFFOrSafari',
  'parseOpera',
  'parseOpera9',
  'parseOpera10',
  'parseOpera11' ]
*/
```

__GIF FTW!__

![error-stack-parser](/images/error-stack-parser/error-stack-parser.gif)

