---
layout: post
title: "emoji-flags"
date: 2019-06-23 09:52:10 +0530
comments: true
categories: fun
---

#[emoji-flags](https://npm.im/emoji-flags)
> emoji flag symbol for a given country code.

`emoji-flags` is a sweet module that returns the emjoi flag for a given country code.


__Get it:__ `npm install emoji-flags`

__Sample usage:__

```js
const emojiFlags = require('emoji-flags');

// single country lookup by code
emojiFlags.countryCode('DK');
// => { "code": "DK", "emoji": "🇩🇰", ... }

// entire dataset
emojiFlags.data;
```

```sh
$ emoji-flags --help

  return emoji flag symbol for country code

  Example
    emoji-flags gb

    emoji-flags dk --verbose

    emoji-flags
    => returns the entire dataset
```

__GIF FTW!__

![emoji-flags](/images/emoji-flags/emoji-flags.gif)
