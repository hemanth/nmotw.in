---
layout: post
title: "sentiment"
date: 2015-10-29 13:17:29 +0000
comments: true
categories: analysis 
---

#[sentiment](https://www.npmjs.com/package/sentiment)
> AFINN-based sentiment analysis.

`Sentiment` uses [AFINN-111](http://www2.imm.dtu.dk/pubdb/views/publication_details.php?id=6010) wordlist to perform [sentiment analysis](http://en.wikipedia.org/wiki/Sentiment_analysis) on arbitrary blocks of input text. 

Sentiment provides serveral things:

- Performance.
- The ability to append and overwrite word / value pairs from the AFINN wordlist.
- A build process that makes updating sentiment to future versions of the AFINN word list trivial.

__Get it:__ `npm install --save sentiment`

__Sample usage:__

```js
> var sentiment = require('sentiment');

> sentiment('Cats are stupid');
{ score: -2,
  comparative: -0.6666666666666666,
  tokens: [ 'cats', 'are', 'stupid' ],
  words: [ 'stupid' ],
  positive: [],
  negative: [ 'stupid' ] }

> sentiment('Cats are cool');
{ score: 1,
  comparative: 0.3333333333333333,
  tokens: [ 'cats', 'are', 'cool' ],
  words: [ 'cool' ],
  positive: [ 'cool' ],
  negative: [] }

> sentiment('Cats are cool',{'cats':5,'cool':10});
{ score: 15,
  comparative: 5,
  tokens: [ 'cats', 'are', 'cool' ],
  words: [ 'cool', 'cats' ],
  positive: [ 'cool', 'cats' ],
  negative: [] }
```

__GIF FTW!__

![sentiment.gif](/images/sentiment/sentiment.gif)

Thanks to [Andrew Sliwinski](https://twitter.com/thisandagain) for this crazy module! 
