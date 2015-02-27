---
layout: post
title: "mute-stream"
date: 2014-07-03 18:32:49 +0530
comments: true
categories: cli 
ogimg: http://nmotw.in/images/mute-stream/mute-stream.gif
---

> Bytes go in, but they don't come out (when muted).

[mute-stream](https://www.npmjs.org/package/mute-stream) as the name says it mutes the stream, as in it's a pass-through stream, but when muted, the bytes are silently dropped, rather than being passed through.

__Installing it:__ `npm install mute-stream`


__Example usage:__

```javascript
var ms = new (require('mute-stream'))({});

ms.pipe(process.stdout);

ms.write('Shout\n');
ms.mute();
ms.write('Shout louder!\n');
ms.unmute();
ms.write('Phew!\n');

```

`({})` is the options part, that can be either of:

* replace => Replaces the muted string with the specified string. (Check the gif)

* prompt =>  prompt with a readline stream, to avoid backspace overwrites.

It also provides `ms.muted()` method to check if the stream is already muted.

> The MuteStream object acts as a facade to its pipe source and destination.

__GIF FTW!__

![](/images/mute-stream/mute-stream.gif)


Thanks to [Isaac Z. Schlueter](http://blog.izs.me/) for helping us to mute the noise! ;)

