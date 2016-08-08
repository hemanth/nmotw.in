---
layout: post
title: "currency-symbol-map"
date: 2016-08-04 11:52:51 +0000
comments: true
categories: util 
---

#[currency-symbol-map](https://www.npmjs.com/package/currency-symbol-map)
> Lookup the currency symbol for a given currency code.

Name says it all, this is tiny module that's helps one to get the symbol for a given currency or get the currency got given a symbol.

__Get it:__ `npm install --save currency-symbol-map`



__Sample usage:__


```js
var getSymbolFromCurrency = require('currency-symbol-map').getSymbolFromCurrency;
getSymbolFromCurrency('USD'); //=> '$' 
getSymbolFromCurrency('NOT A VALID CODE'); //=> undefined 
```


```js
var getCurrencyFromSymbol = require('currency-symbol-map').getCurrencyFromSymbol;
getCurrencyFromSymbol('$'); //=> 'USD' 
getCurrencyFromSymbol('NOT A VALID CODE'); //=> undefined 
```


__GIF FTW:__


![currency-symbol-map](/images/currency-symbol-map/curreny-symbol-map.gif)
