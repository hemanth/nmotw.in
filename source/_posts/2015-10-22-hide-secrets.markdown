---
layout: post
title: "hide-secrets"
date: 2015-10-22 14:09:43 +0000
comments: true
categories: util
---
<script src="https://embed.tonicdev.com" data-element-id="hide-secrets"></script>

#[hide-secrets](https://www.npmjs.com/package/hide-secrets)
> hide certain restricted fields whiling logging objects.

This module obfuscated any of `password`, `pass`, `token`, `auth`, `secret` or `passphrase` attribute's value to `'[SECRET]'`.
Very useful when logging an object that has sensitive data!

__Install it:__ ```npm install --save hide-secrets```

__Sample usage:__

<div id="hide-secrets">
var hide = require('hide-secrets')
 
var obj = {
  innerObject: {
    password: 'abc123',
    email: 'xyz@nmotw.in',
    token: 'my-secret-token'
  },
  auth: '' // empty strings are left empty. 
}
 
hide(obj)
</div>

__GIF FTW!__

![hide-secrets](/images/hide-secrets/hide-secrets.gif)


Thanks to [Benjamin Coe](https://twitter.com/benjamincoe) for helping us hide our secrets ;)
