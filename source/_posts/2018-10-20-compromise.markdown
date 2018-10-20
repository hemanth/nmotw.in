---
layout: post
title: "compromise"
date: 2018-10-20 14:26:13 +0530
comments: true
categories: nlp
---

#[compromise](https://npm.im/compromise)
> modest natural-language processing.

`compromise` is not the cleverest, but it is small, quick, and good-enough for a bunch of nlp stuff!

Don't miss to checkout their site [compromise.cool](http://compromise.cool/)!

__GET IT:__ `npm install compromise`

__Sample usages:__

```js

const nlp = require('compromise')

const doc = nlp('JS is calling')
doc.sentences().toNegative()
// 'JS is not calling'

```

```js
doc = nlp("the guest-singer's björk   at seven thirty.").normalize().out('text')
// 'The guest singer is Bjork at 7:30.'
```

```js
doc = nlp("we're not gonna take it, no we ain't gonna take it.")
doc.has('going') // true
doc.match('are not').length // == 2
doc.contractions().expand().out()
//'we are not going to take it, no we are not going to take it'
```

__GIT FTW!__

![compromise.gif](/images/compromise/compromise.gif)