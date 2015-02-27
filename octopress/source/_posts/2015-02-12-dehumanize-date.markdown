---
layout: post
title: "dehumanize-date"
date: 2015-02-12 17:57:21 +0530
comments: true
categories: util
---

# [dehumanize-date](https://www.npmjs.com/package/dehumanize-date)
> Parse dates in all the formats humans like to use.

Yes, it dehumanize dates will almost all the formates humans like to use, those invovle:


 - today/tomorrow/yesterday
 - next/this/last Wednesday
 - 12th January
 - 12th January 1950
 - 09-08-2008
 - 2008-08-09

And returns a computer friendly date of the format: `yyyy-dd-mm`

The heart of the module consists of the below regular expressions:

```js
var NUMBER              = /^[0-9]+$/;
var NUMBER_WITH_ORDINAL = /^([0-9]+)(st|nd|rd|th)?$/;
var NUMBER_DATE         = /^(3[0-1]|[1-2][0-9]|0?[1-9])[,\|\\\/\-\. ]+(1[0-2]|0?[1-9])[,\|\\\/\-\. ]+([0-9]{4})$/;
var NUMBER_DATE_USA     = /^(1[0-2]|0?[1-9])[,\|\\\/\-\. ]+(3[0-1]|[1-2][0-9]|0?[1-9])[,\|\\\/\-\. ]+([0-9]{4})$/;
var NUMBER_DATE_SHORT_YEAR         = /^(3[0-1]|[1-2][0-9]|0?[1-9])[,\|\\\/\-\. ]+(1[0-2]|0?[1-9])[,\|\\\/\-\. ]+([0-9]{2})$/;
var NUMBER_DATE_SHORT_YEAR_USA     = /^(1[0-2]|0?[1-9])[,\|\\\/\-\. ]+(3[0-1]|[1-2][0-9]|0?[1-9])[,\|\\\/\-\. ]+([0-9]{2})$/;
var ISO_8601_DATE       = /^([0-9]{4})-?(1[0-2]|0?[1-9])-?(3[0-1]|[1-2][0-9]|0?[1-9])$/;
```

__Sample usage:__

```js
> var dehumanizeDate = require('dehumanize-date');

> dehumanizeDate
{ [Function: parse]
  parseNearbyDays: [Function: parseNearbyDays],
  parseLastThisNext: [Function: parseLastThisNext],
  parseNumberDate: [Function: parseNumberDate],
  parseNumberDateShortYear: [Function: parseNumberDateShortYear],
  parseWordyDate: [Function: parseWordyDate],
  monthFromName: [Function: monthFromName],
  date: [Function: date] }


> dehumanizeDate("today")
'2015-02-12'

> dehumanizeDate("tommorrow") // In case it does not match any.
null

> dehumanizeDate("tomorrow")
'2015-02-13'

> dehumanizeDate("yesterday")
'2015-02-11'

> dehumanizeDate("1st January")
'2015-01-01'

> dehumanizeDate("1st January 1997")
'1997-01-01'

> dehumanizeDate("09-09-2009")
'2009-09-09'

> dehumanizeDate("2009-09-09")
'2009-09-09'

```

__GIF FTW!__

![dehumanize-date](/images/dehumanize-date/dehumanize-date.gif)

Thanks for [Forbes Lindesay](http://www.jepso.com) for dehumanizing dates ;)

