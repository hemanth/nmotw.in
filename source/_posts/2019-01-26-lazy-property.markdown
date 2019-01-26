---
layout: post
title: "lazy-property"
date: 2019-01-26 14:08:16 +0530
comments: true
categories: util functional
---

#[lazy-property](https://www.npmjs.com/package/lazy-property)
> Add a lazily initialized property to an object.

`lazy-propert` play well with `Object.defineProperty` to provide laziness over object's properties. 

__Get it:__ `npm install lazy-property`

__Sample usage:__

```js
require("lazy-property")(obj, name, init[, enumerable])
```

^ Adds a lazily initialized property to the object.

* `obj` is the object to add the property to
* `name` is the name of the property
* `init` is a function that computes the value of the property
* `enumerable` if the property is enumerable (default false)

```js
var addLazyProperty = require("lazy-property")

var obj = {}

addLazyProperty(obj, "foo", function() {
  console.log("initialized!")
  return "bar"
})

//Access the property
console.log(obj.foo)
console.log(obj.foo)

//Prints out:
//
//    initialized!
//    bar
//    bar
//
```

__GIF FTW!__

![lazy-property](/images/lazy-property/lazy-property.gif)
