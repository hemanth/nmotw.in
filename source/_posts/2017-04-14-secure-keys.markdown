---
layout: post
title: "secure-keys"
date: 2017-04-14 10:41:06 +0000
comments: true
categories: crypto
---

#[secure-keys](https://www.npmjs.com/package/secure-keys)
>Encrypts and Decrypts object keys.

This module uses node's inbuilt `crypto` to encrypt and decrypt object keys and the code was yanked out of work by
[@indexzero](https://github.com/indexzero) for [`nconf`](https://github.com/indexzero/nconf)

__Get it:__ `npm install --save secure-keys`

__Sample usage:__

```js
const secureKeys = require("secure-keys")

const sk = new secureKeys({secret: 'NOTW'});
const enCat = sk.encrypt({cat: 'meow'})
const deCat = sk.decrypt(enCat);

console.log('encrypted object:', enCat);

console.log('decrypted object:', deCat);

/*
encrypted object: { cat: { alg: 'aes-256-ctr', value: '3f1ead878c36' } }

decrypted object: { cat: 'meow' }
*/
```

```js
var sec = new SecK({
  secret: 'BEGIN RSA', // Text of key used for encrypting/decrypting 
  format: JSON, // optional (defaults to JSON): An object with `stringify` and `parse` methods 
  alg: 'aes-256-ctr' //optional (this is default) Algorithm to use for encrypt/decrypt 
});
```

__GIF FTW!__

![](/images/secure-keys/secure-keys.gif)


