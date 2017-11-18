---
layout: post
title: "webtorrent-element"
date: 2017-11-16 16:09:50 +0530
comments: true
categories: html
---

[webtorrent-element](https://npmjs.com/package/webtorrent-element)
> webcomponent for torrents.

You would not really appreciate this module if you haven't read [I’ve seen the future, it’s full of HTML.](https://medium.com/@mikeal/ive-seen-the-future-it-s-full-of-html-2577246f2210)

This module makes use of `webtorrent` to implement an HTML element you can use to display content on WebTorrent.

__Get it:__ `npm install --save webtorrent-element`

__Sample usage:__

```js
// This gets bundled.
const WebTorrentComponent = require('webtorrent-element');

let elem = new WebTorrentComponent();
elem.src = MAGNETURL; // MANGETURL to be viewed.
elem.file = 'Sintel.mp4'; // File in that torrent.
document.body.appendChild(elem);
```

__GIF FTW!__

![webtorrent-element](/images/webtorrent-element/webtorrent-element.gif)




