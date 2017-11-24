---
layout: post
title: "clean-deep"
date: 2017-11-23 11:12:26 +0530
comments: true
categories: util
---

#[clean-deep](https://www.npmjs.com/package/clean-deep)
> Remove empty values from objects.

`clean-deep` helps us to clean objects by removing empty `[]`, `{}`, `null`, `undefined`, `''` from objects.

Around of 50 lines of code which makes use of `lodash.transform` and recursively clean up your objects.

You could pass in the below options as per your requirement of the clean-up process.


Option            | Default value | Description
----------------- | ------------- | -----------------------------------
_emptyArrays_     | _true_        | Remove empty arrays, ie: `[]`
_emptyObjects_    | _true_        | Remove empty objects, ie: `{}`
_emptyStrings_    | _true_        | Remove empty strings, ie: `''`
_nullValues_      | _true_        | Remove null values, ie: `null`
_undefinedValues_ | _true_        | Remove null values, ie: `undefined`


__Get it:__ `npm install clean-deep`

__Sample usage:__

```javascript
const cleanDeep = require('clean-deep');
const object = {
  bar: {},
  baz: null,
  biz: 'baz',
  foo: '',
  net: [],
  nit: undefined,
  qux: {
    baz: 'boz',
    txi: ''
  }
};

cleanDeep(object);
// => { biz: 'baz', qux: { baz: 'boz' } }
```

__GIF FTW!__

![clean-deep](/images/clean-deep/clean-deep.gif)

