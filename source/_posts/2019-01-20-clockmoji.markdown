---
layout: post
title: "clockmoji"
date: 2019-01-20 20:00:13 +0530
comments: true
categories: util fun
---

#[clockmoji](https://www.npmjs.com/package/clockmoji)
> 🕗 Get an emoji clock based on the time.

`clockmoji` is fun little module for representation of the current time in emoji.

It calculates the short hard, long hard for the clock and fetch the required emoji's unicode.

```js
  var date = new Date(date.getTime() + 15 * 60000)
  var shortHand = date.getHours() % 12
  var min = date.getMinutes()
  var longHand = (min - (min % 30)) / 30 ? '30' : '00'
```

__Get it:__ `npm install clockmoji`

__Sample usage:__

```js
date
Tue May 26 18:19:10 CDT 2015

# no arguments will return the current time
clockmoji
🕡

# Pass a time in the format mm:ss
clockmoji 10:00
🕙

# Military time supported
clockmoji 14:00
🕑

# any arbitrary time works -- rounds down if its less than :15
clockmoji 12:04
🕛

# rounds up if the minutes are :15
clockmoji 12:24
🕧

# supports piping
echo 6:30 | clockmoji
🕡

# invalid time returns ⚠
clockmoji 9999
⚠
```

```js
const clockmoji = require('clockmoji')

console.log(clockmoji())
console.log(clockmoji('12:00'))
console.log(clockmoji('18:30'))
```


__GIF FTW!__

![clockmoji](/images/clockmoji/clockmoji.gif)
