---
layout: post
title: "sentencer"
date: 2015-02-19 19:15:03 +0530
comments: true
categories: fun 
---

#[sentencer](https://www.npmjs.com/package/sentencer)
> Templating engine for madlibs-style sentence generating.

Create crazy sentences with `nouns`, `adjectives` and your own randomness! 

`Sentencer` was written for and powers [Metaphorpsum](http://metaphorpsum.com). The noun and adjective lists for form -> [Word Lists for Writers](http://www.ashley-bovan.co.uk/words/partsofspeech.html).

__Install it:__ `npm install sentencer --save`

__Sample usage:__

```js

const Sentencer = require('sentencer');

let str = " A {{noun}} jumped over {{an_adjective}}";

Sentencer.make(str); //' A agreement jumped over a sprightful'

Sentencer.make(str); // ' A shrine jumped over a wordless'

str = " {{a_noun}} jumped over {{an_adjective}}";

Sentencer.make(str); // ' an instruction jumped over a scabrous'
Sentencer.make(str); // ' a thistle jumped over a shapely'

```

__Define custom actions:__

```js
Sentencer.configure({
  actions: {
    rand: function() {
      return Math.floor( Math.random()  * 10 );
    }
  }
});

Sentencer.make("I like {{rand}}"); // 'I like 7'
```

__GIF FTW:__

![sentencer](/images/sentencer/sentencer.gif)


Thanks to [@kylestetz](https://twitter.com/kylestetz) for this fun module! (:

