---
layout: post
title: "breakable"
date: 2017-10-12 17:39:52 +0530
comments: true
categories: util
---

#[breakable](https://www.npmjs.com/package/breakable)
> Break out of functions in a more composable way.

`breakable` is useful when you want to break out of a deep recursion, passing a value, without riddling your code with exception ceremony.

__Get it:__ `npm install breakable`

__Sample usage:__

Instead of

```js
const esprima = require("esprima").parse;
const traverse = require("ast-traverse");
const ast = esprima("f(!x, y)");
 
let val;
try {
    traverse(ast, {pre: function(node) {
        if (node.type === "UnaryExpression" && node.operator === "!") {
            val = node.argument;
            throw 0;
        }
    }});
} catch(e) {
    if (val === undefined) {
        throw e; // re-throw if it wasn't our exception 
    }
}
 
console.dir(val); // { type: 'Identifier', name: 'x' } 
```

You could:

```js
const breakable = require("breakable");
const esprima = require("esprima").parse;
const traverse = require("ast-traverse");
const ast = esprima("f(!x, y)");
 
const val = breakable(function(brk) {
    traverse(ast, {pre: function(node) {
        if (node.type === "UnaryExpression" && node.operator === "!") {
            brk(node.argument);
        }
    }});
});
 
console.dir(val); // { type: 'Identifier', name: 'x' } 
```

__GIF FTW__

![breakable](/images/breakable/breakable.gif)

P.S: This is a trivial example, if you want to do something like that in the `gif` you might want `.some`


