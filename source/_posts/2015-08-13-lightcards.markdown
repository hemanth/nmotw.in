---
layout: post
title: "lightcards"
date: 2015-08-13 14:06:54 +0000
comments: true
categories: learn fun
---

#[lightcard](https://www.npmjs.com/package/lightcards)
> Lightweight Chinese flashcards.

`lightcards` is one of those lightweight, single purpose, fun modules! This helps you to make flash cards that would help you to learn Chinese characters!
By default, lightcards uses vocabulary.txt from the current working directory. If no `vocabulary.txt` can be found, lightcards will create it create it for you,
after which it will start a minimalistic server with a cute interface to go through the  list of word that was provided from a file or stdin.

__Get it__: `npm install -g lightcards`

__Simple usage:__

```sh
$ lightcards init && lightcards

Reading vocabulary from vocabulary.txt... OK!
Generating flashcards... OK!
Compiling scripts... OK!
Starting local web server... OK!

Start learning on http://localhost:3000
```

__GIF FTW!__

![lightcards](/images/lightcards/lightcards.gif)

Thanks to [Oscar Söderlund](https://github.com/odsod) for `lightcards`!
