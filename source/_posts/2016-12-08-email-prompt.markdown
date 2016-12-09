---
layout: post
title: "email-prompt"
date: 2016-12-08 13:14:32 +0000
comments: true
categories: cli
---

#[email-prompt](https://www.npmjs.com/package/email-prompt)
> CLI email prompt featuring autocompletion and validation.

`email-prompt` Powers 𝚫now --login and provides a nice promised based API for email autocompletion and validation.

It's customiziable with the below options:

```js
{
  start :'> Enter your email: ',
  domains :new Set([
    'aol.com',
    'gmail.com',
    'google.com',
    'yahoo.com',
    'ymail.com',
    'hotmail.com',
    'live.com',
    'outlook.com',
    'inbox.com',
    'mail.com',
    'gmx.com',
    'icloud.com'
  ]),
  forceLowerCase :true,
  suggestionColor :'gray',
  autoCompleteChars :new Set([
    '\t' /* tab */,
    '\r' /* return */,
    '\x1b[C' /* right arrow */,
    ' ' /* spacebar */
  ]),
  resolveChars :new Set(['\r']),
  abortChars :new Set(['\x03']),
  allowInvalidChars :false
} 
```

__Get it:__ `npm install --save email-prompt`

__Sample usage:__

```js

const prompt = require('email-prompt');
prompt({ /* opts */ })
.then((email) => {
  console.log('\n> Hello ' + val);
))
.catch(() => {
  console.log('\n> Aborted!');
})

```

__Important to note:__

- `email-prompt` automatically adapts the mode of `process.stdin` for you.
- The `stdin` stream is `resume`d and `pause`d upon the promise being
  settled.
- When the promise resolves or rejects, the previous stdin mode is restored.
- The `tty` mode is set to `raw`, which means all the caret interactions
  that you come to expect in a regular `stdin` prompt are simulated.
  This gives us fine-grained control over the output and powers the
  validation.


__GIF FTW!__

![email-prompt](/images/email-prompt/email-prompt.gif)

