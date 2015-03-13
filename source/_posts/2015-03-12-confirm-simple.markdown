---
layout: post
title: "confirm-simple"
date: 2015-03-12 15:24:10 +0000
comments: true
categories: CLI util
---

#[confirm-simple](http://npm.im/confirm-simple)
> A simple command-line tool to confirm.

If you have written CLI apps, you would have for sure come across a senario of taking an action based on the users choice. 

`confirm-simple` as the name says it's a simple to use util that would help you to confirm users choice with ease.

__Install it:__ `npm install --save confirm-simple`

__API and simple usage:__

```js
var confirm = require('confirm-simple')

confirm('Do you accept the EULA?', ['yes', 'no'] ,function (yes) {
    if (yes) { 
      console.log('Good for you!');
    } else {
      console.log('Sorry you wont get to use the software');
    }
});
```

__GIF FTW!__

![](/images/confirm-simple/confirm-simple.gif)

Thanks to YouBao Nong for `confirm-simple`.