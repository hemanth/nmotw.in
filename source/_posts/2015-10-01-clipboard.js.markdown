---
layout: post
title: "clipboard.js"
date: 2015-10-01 12:50:14 +0000
comments: true
categories: util html dom
alias: [/clipboard.js/index.html]
---

#[clipboard.js](http://zenorocha.github.io/clipboard.js/)
> A modern approach to copy text to clipboard!

With 4.7K+ stars to it's repo with a modern approach to copy text coded with `ES2015/6` classes,  No Flash. Just 2kb! 

[Zeno Rocha](http://zenorocha.com/)'s `clipboard.js` undoubtedly is the nmotw! 

It makes use of  [Selection](https://developer.mozilla.org/en-US/docs/Web/API/Selection) and [execCommand](https://developer.mozilla.org/en-US/docs/Web/API/Document/execCommand) APIs.

__Get it:__ ```npm install --save clipboard.js```

__Sample usage:___

```js
var clipboard = new Clipboard('.btn');

clipboard.on('success', function(e) {
    console.info('Action:', e.action);
    console.info('Text:', e.text);
    console.info('Trigger:', e.trigger);

    e.clearSelection();
});

clipboard.on('error', function(e) {
    console.error('Action:', e.action);
    console.error('Trigger:', e.trigger);
});
```

In your `HTML`:

```html
<!-- Target -->
<input id="foo" value="https://github.com/zenorocha/clipboard.js.git">

<!-- Trigger -->
<button class="btn" data-clipboard-target="#foo">
    <img src="assets/clippy.svg" alt="Copy to clipboard">
</button>
```

__GIF FTW!__

![clipboard.js](/images/clipboard.js/clipboard.js.gif)



