---
layout: post
title: "combokeys"
date: 2015-07-23 14:32:46 +0000
comments: true
categories: dom event 
---

[combokeys](https://www.npmjs.com/package/combokeys)
> Handles keyboard shortcuts in the browser.

`combokeys` is a fork of [ccampbell/mousetrap](https://github.com/ccampbell/mousetrap) with two main changes:

* Refactored as CommonJS
* Doesn't automatically listen on the document. Instead, it is now a constructor and the element on which to listen must be provided on instantiation.

__Install it:__ ``` npm install --save combokeys ```

__Sample usage:__


```js
var Combokeys = require("combokeys");
var Mousetrap = new Combokeys(document.documentElement);
// Or, instantiate it for one or more specific elements:
var firstCombokeys = new Combokeys(document.getElementById("first"));

firstCombokeys.bind('4', function() { console.log('4'); });
firstCombokeys.bind("?", function() { console.log('show shortcuts!'); });

```

__GIF FTW!__

![combokeys](/images/combokeys/combokeys.gif)

