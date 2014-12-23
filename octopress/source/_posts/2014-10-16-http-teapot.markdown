---
layout: post
title: "http-teapot"
date: 2014-10-16 18:53:28 +0530
comments: true
categories: fun
ogimg: http://nmotw.in/images/http-teapot/http-teapot.gif
---

# [http-teapot](https://www.npmjs.org/package/http-teapot)

Add support for [RFC 2324](https://www.ietf.org/rfc/rfc2324.txt) to any HTTP server.

P.S:  Hyper Text Coffee Pot Control Protocol (HTCPCP/1.0) was a April fools RFC ;) HTTP status code `418`.

BTW if you are wondering why this made in to this list, `http-teapot` module is the 100,000th module to npm today!

<blockquote class="twitter-tweet" lang="en"><p>congrats to <a href="https://twitter.com/wa7son">@wa7son</a> who published the 100,000th module to npm today, a http 418 teapot protocol implementation <a href="http://t.co/ckKrSizu9Q">pic.twitter.com/ckKrSizu9Q</a></p>&mdash; maxwell ogden (@maxogden) <a href="https://twitter.com/maxogden/status/522413667782914048">October 15, 2014</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

## Installation

```sh
npm install http-teapot
```

## Usage

Just add http-teapot as a routing function.

Express example:

```javascript
var teapot = require('http-teapot');
var express = require('express');
var app = express();

app.get('/teapot', teapot);

app.listen(3000);
```

__GIF FTW!__

![http-teapot](/images/http-teapot/http-teapot.gif)


Thanks to [Thomas Watson Steen](https://github.com/watson) for implementing this RFC and giving us a teapot image ;)
