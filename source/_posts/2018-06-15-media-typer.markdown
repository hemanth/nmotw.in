---
layout: post
title: "media-typer"
date: 2018-06-15 16:35:15 +0530
comments: true
categories: util 
---

#[media-typer](https://npm.im/media-typer)
> RFC 6838 media type parser.

`media-typer` helps in parsing and formatting media type.

__Get it:__ `npm install media-typer`

__Sample usage:__

```js
const typer = require('media-typer');

typer.parse('image/svg+xml; charset=utf-8');

/*
{ type: 'image',
  subtype: 'svg',
  suffix: 'xml',
  parameters: { charset: 'utf-8' } 
}
*/

typer.format({type: 'image', subtype: 'svg', suffix: 'xml'})

// ^ 'image/svg+xml'
```

```js
typer.parse(req);

/* ^ Parse the `content-type` header from the given req.
 Short-cut for typer.parse(req.headers['content-type'])*/
```

__GIF FTW!__

![media-typer](/images/media-typer/media-typer.gif)

