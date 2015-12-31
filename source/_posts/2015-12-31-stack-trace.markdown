---
layout: post
title: "stack-trace"
date: 2015-12-31 17:47:09 +0000
comments: true
categories: debug trace
---

#[stack-trace](https://www.npmjs.com/package/stack-trace)
> Get v8 stack traces as an array of CallSite objects.

__Get it:__ `npm install --save stack-trace`

__Sample usage:__

```js
var stackTrace = require('stack-trace');
var trace = stackTrace.get();
```

```js
var stackTrace = require('stack-trace');
var err = new Error('something went wrong');
var trace = stackTrace.parse(err);
```

And `trace` would have CallSite objects and each object will have the below methods:

* **getThis**: returns the value of this
* **getTypeName**: returns the type of this as a string. This is the name of the function stored in the constructor field of this, if available, otherwise the object's [[Class]] internal property.
* **getFunction**: returns the current function
* **getFunctionName**: returns the name of the current function, typically its name property. If a name property is not available an attempt will be made to try to infer a name from the function's context.
* **getMethodName**: returns the name of the property of this or one of its prototypes that holds the current function
* **getFileName**: if this function was defined in a script returns the name of the script
* **getLineNumber**: if this function was defined in a script returns the current line number
* **getColumnNumber**: if this function was defined in a script returns the current column number
* **getEvalOrigin**: if this function was created using a call to eval returns a CallSite object representing the location where eval was called
* **isToplevel**: is this a toplevel invocation, that is, is this the global object?
* **isEval**: does this call take place in code defined by a call to eval?
* **isNative**: is this call in native V8 code?
* **isConstructor**: is this a constructor call?

__GIF FTW__

![stack-trace](/images/stack-trace/stack-trace.gif)
