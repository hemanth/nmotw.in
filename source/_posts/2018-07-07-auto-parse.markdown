---
layout: post
title: "auto-parse"
date: 2018-07-07 21:59:37 +0530
comments: true
categories: util 
---

#[auto-parse](https://www.npmjs.com/package/auto-parse)
> auto-parse any value you happen to send in.

`auto-parse` any value you happen to send in like: `String`, `Number`, `Boolean`, `Array`, `Object`, `Function`, `undefined` and `null` and it shall get parsed to the appropriate value.

__GET IT:__ `npm install auto-parse`

__Sample usage:__

```js

const autoParse = require("auto-parse")

autoParse([
  '1', 'TrUe', ' undefined ', 
  ' null ', '[]', {age : "50"}
]);

/*

[1, true, undefined, null, [], {age: 50} ]

*/

```

```js

// Set Type
autoParse(1, 'Boolean')  =>  true
autoParse(0, 'Number')  =>   0
autoParse(1, Boolean)  =>  true
autoParse(0, Number)  =>   0
autoParse(1234, String)  =>  '1234'

```

```js
// dates
autoParse('1989-11-30', 'date')  =>  Thu Nov 30 1989 18:00:00 GMT-0600 (CST)
autoParse('1989-11-30', Date)  =>  Thu Nov 30 1989 18:00:00 GMT-0600 (CST)
```

```js
// Passing Functions to type
function Color (inputColor) {
  this.color = inputColor
}
autoParse('#AAA', Color)  =>  {color: '#AAA'}
```

__GIF FTW!__

![auto-parse](/images/auto-parse/auto-parse.gif)