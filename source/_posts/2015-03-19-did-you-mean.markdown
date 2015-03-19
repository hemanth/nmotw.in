---
layout: post
title: "did-you-mean"
date: 2015-03-19 12:11:21 +0000
comments: true
categories: util
---

#[did-you-mean](https://www.npmjs.com/package/did-you-mean)
>Fuzzy match a command from a list (typo-safety)

This module does a Fuzzy match a word from your list of commands or keywords from node.js/io.js to provide a friendly typo-safe human prompt.

__Install it:__ `npm install --save did-you-mean`

__API:__

* get -> Get the closest match.
 
* setThreshold(3) -> Set the threshold (the maximum Levenshtein distance)

* list('key') -> List all matches.
 
* ignoreCase() -> Set ignore case.

* matchCase() -> Set match case.

* add('key1','key2',...); -> Add more values.

__Usage:__

```js
var Matcher = require('did-you-mean');

var m = new Matcher('init install update upgrade npm brew apt-get');

m.get('upgarde'); // "upgrade"

m.get('brwe'); // "brew"

m.get('atp-get'); // "apt-get"

m.values; // ["npm", "brew", "upgrade", "update", "apt-get"]

m.list('upgarde'); // {distance: 2, value: "upgrade"}
```

__GIF FTW!__

![did-you-mean](/images/did-you-mean/did-you-mean.gif)

Thanks to Boris Okunskiy for bringing `did-you-mean` to web and CLI.
