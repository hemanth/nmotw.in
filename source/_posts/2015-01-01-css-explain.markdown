---
layout: post
title: "css-explain"
date: 2015-01-01 18:53:53 +0530
comments: true
categories: learn 
---

#[css-explain](https://www.npmjs.com/package/css-explain)
> Think of it like SQL EXPLAIN, but for CSS selectors.

`css-explain` is one of such rare modules that helps us to learn or explain CSS selectors with ease.

__Get it:__ `npm install css-explain`

__Sample usage:__

```javascript
> var cssExplain = require('css-explain').cssExplain

> cssExplain("div .info")
{ selector: 'div .info',
  parts: [ 'div', '.info' ],
  category: 'class',
  key: 'info',
  specificity: [ 0, 1, 1 ],
  score: 6,
  messages: [ 'Uses a descendant selector with a rightmost class selector' ] }

> cssExplain("div#info")
{ selector: 'div#info',
  parts: [ 'div#info' ],
  category: 'id',
  key: 'info',
  specificity: [ 1, 0, 1 ],
  score: 2,
  messages: [ 'ID is overly qualified by a tag name' ] }

> cssExplain("div > p#info")
{ selector: 'div > p#info',
  parts: [ 'div', '>', 'p#info' ],
  category: 'id',
  key: 'info',
  specificity: [ 1, 0, 2 ],
  score: 3,
  messages: 
   [ 'ID is overly qualified by a tag name',
     'ID is overly qualified by a child selector' ] }

```

__GIF FTW!__

![css-explain](/images/css-explain/css-explain.gif)


Thanks to [Joshua Peek](https://twitter.com/joshpeek) for css-explain, do [checkout](http://josh.github.io/css-explain/) the webbased app of the same.