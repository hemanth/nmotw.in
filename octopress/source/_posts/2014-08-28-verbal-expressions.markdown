---
layout: post
title: "verbal-expressions"
date: 2014-08-28 22:14:18 +0530
comments: true
categories: util
ogimg: http://nmotw.in/images/verbal-expressions/verba-expressions.gif
---

> JavaScript Regular Expressions made easy

[VerbalExpressions](https://www.npmjs.org/package/verbal-expressions) helps us to construct difficult regular expressions is an intuitive manner.

__Install it:__ `npm install verbal-expressions`


__Example usage:__

```javascript
var ve = require('verbal-expressions');
var url = "http://nmotw.in";
var vre = ve()
	.startOfLine()
	.then( 'http' )
	.maybe( 's' )
	.then( '://' )
	.maybe( 'www.')
	.anythingBut( " " )
	.endOfLine();

vre.test(url); //true

vre.toRegExp(); // /^(?:http)(?:s)?(?:\:\/\/)(?:www\.)?(?:[^\ ]*)$/gm
```

__What else do we have?__

Modifiers:

* anything()

* anythingBut( value )

* endOfLine()

* find( value )

* maybe( value )

* startOfLine()

* then( value )

Special characters and groups:

* any( value )

* anyOf( value )

* br()

* lineBreak()

* range( from, to)

* tab()

* word()

Modifiers:

* withAnyCase()

* stopAtFirst()

* searchOneLine()

Functions:

* replace( source, value )

Others:

* add( expression )

* multiple( value )

* or()


__GIF FTW!__

![](/images/verbal-expressions/verbal-expressions.gif)


Thanks to __Mihai Ionut Vilcu__ for verbal expressions!