---
layout: post
title: "captionbot"
date: 2016-05-05 12:57:22 +0000
comments: true
categories: bot
---

[captionbot](https://www.npmjs.com/package/captionbot)
> Get captions for image using Microsoft's CaptionBot 🤖

A cheeky bot that tries recognize an image and explain it like a human would do, it requires node version `>=4` this is powered by [CaptionBot](https://www.captionbot.ai/), a free service provided by Microsoft.

The author says he would consider this module "for testing only" and does not recommend using in a production system.

__Get it:__ `npm install --save captionbot`

__Usage:__

```js
const captionbot = require('captionbot');

captionbot('http://i.imgur.com/o33PTUp.jpg')
.then(caption => {
    console.log(caption);
});

//=> 'I think it's a group of people posing for a picture\nand he seems 😐.'
```

or 

```js
const captionbot = require('captionbot');

try {
    const caption = await captionbot('http://i.imgur.com/o33PTUp.jpg');
    console.log(caption);
} catch(e) {
    console.error(e);
}
```

__GIF FTW!__

![](/images/captionbot/captionbot.gif)

