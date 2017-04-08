---
layout: post
title: "what-input"
date: 2017-04-07 14:10:55 +0000
comments: true
categories: dom
---

[what-input](https://www.npmjs.com/package/what-input)
> A global utility for tracking the current input method (mouse, keyboard or touch).

What Input adds data attributes to the <html> tag based on the type of input being used. 

It also exposes a simple API that can be used for scripting interactions.

__GET IT:__ `npm install --save what-input`

__Sample usage:__

```js
whatInput.ask(); // returns `mouse`, `keyboard` or `touch`

whatInput.types(); // ex. returns ['mouse', 'keyboard']

whatInput.ask('loose'); // returns `mouse` because mouse movement was detected

myButton.addEventListener('click', function() {

  if (whatInput.ask() === 'mouse') {
    // do mousy things
  } else if (whatInput.ask() === 'keyboard') {
    // do keyboard things
  }

});
```



Event mapping:

```js
// mapping of events to input types
const inputMap = {
    'keyup': 'keyboard',
    'mousedown': 'mouse',
    'mousemove': 'mouse',
    'MSPointerDown': 'pointer',
    'MSPointerMove': 'pointer',
    'pointerdown': 'pointer',
    'pointermove': 'pointer',
    'touchstart': 'touch'
};
```

__GIF FTW:__

![what-input](/images/what-input/what-input.gif)
