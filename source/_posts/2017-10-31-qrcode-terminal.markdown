---
layout: post
title: "qrcode-terminal"
date: 2017-10-31 12:56:26 +0530
comments: true
categories: cli
---

[qrcode-terminal](https://www.npmjs.com/package/qrcode-terminal)
> qrcode on terminal.

`qrcode-terminal` Going where no QRCode has gone before ;)

Helps you to generate qrcode in your terminal, maybe be URLs or just plain text, this module does a good job in displaying the qrcode on terminal. 

It would be great if this module can generate responsive qr-code in the terminal, which can be bit of a challenge, it can generate `small` or `normal` ones though.

__Get it:__ `npm install qrcode-terminal`

__Sample usage:__

```js
const qrcode = require('qrcode-terminal');

qrcode.generate('This will be a QRCode, eh!');

qrcode.setErrorLevel('Q');
qrcode.generate('This will be a QRCode with error level Q!');

qrcode.generate('https://nmotw.in', function (qrcode) {
    console.log(qrcode);
});
```

__GIF FTW!__

![qrcode-terminal](/images/qrcode-terminal/qrcode-terminal.gif)


