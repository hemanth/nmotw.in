---
layout: post
title: "trymodule"
date: 2016-03-31 13:11:49 +0000
comments: true
categories: cli util npm 
---

#[trymodule]()
>It's never been easier to try nodejs modules!

Quickly install any node module you want and start a `REPL` with the installed module in the scope with `trymodule`!

Basically, it check if the module you are trying exists in the `~/.trymodule/node_module` if require it and start a `REPL` or 
else installs it using `npmi` module and starts the `REPL`.

__Get it:__ `npm install -g trymodule`

__Sample usage:__

```sh
nmotw.in> trymodule xkcd-imgs
Gonna start a REPL with packages installed and loaded for you
Couldn't find 'xkcd-imgs' locally, gonna download it now
xkcd-imgs@1.0.1 ../../Users/hhegadehallimadh/.trymodule/node_modules/xkcd-imgs
└── request@2.69.0 (aws-sign2@0.6.0, forever-agent@0.6.1, tunnel-agent@0.4.2, oauth-sign@0.8.1, caseless@0.11.0, is-typedarray@1.0.0, stringstream@0.0.5, isstream@0.1.2, json-stringify-safe@5.0.1, extend@3.0.0, tough-cookie@2.2.2, node-uuid@1.4.7, qs@6.0.2, mime-types@2.1.10, form-data@1.0.0-rc4, combined-stream@1.0.5, hawk@3.1.3, aws4@1.3.2, http-signature@1.1.1, bl@1.0.3, har-validator@2.0.6)
Package 'xkcd-imgs' was loaded and assigned to 'xkcd_imgs' in the current scope
REPL started...
> 
```

```js
> xkcd_imgs
{ img: [Function] }
> xkcd_imgs.img( (err, res) => console.log(res) );
undefined
> { url: 'http://imgs.xkcd.com/comics/instagram.png',
  title: 'I\'m gonna call the cops and get Chad arrested for theft, then move all my stuff to the house across the street. Hopefully the owners there are more responsible.' }
```

__GIF FTW!__

![trymodule](/images/trymodule/trymodule.gif)



