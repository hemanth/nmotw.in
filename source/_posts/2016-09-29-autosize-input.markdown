---
layout: post
title: "autosize-input"
date: 2016-09-29 14:00:53 +0000
comments: true
categories: html
---

#[autosize-input](https://www.npmjs.org/package/autosize-input)
> Effortless, dynamic-width text boxes.

__Features:__

- Dynamically adjusts the width of the text box to fit its current contents
- Can be initialised to fit its `placeholder` attribute
- Optionally set a `min-width` based on the element&rsquo;s initial content

__Get it:__ `npm install -g autosize-input`

__Usage:__

```js
autosizeInput(document.querySelector('#foo'));

autosizeInput(document.querySelector('#bar'));

autosizeInput(document.querySelector('#baz'), { minWidth: true });
```

__Implementation details:__

- The [`box-sizing`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing) property of the given text box is set, inline, to `content-box`. Therefore, the width we assign to our text box *excludes* its `padding` and `border` properties.

- A hidden &ldquo;ghost&rdquo; `div` &mdash; given the same `font-size` and `font-family` as the text box &mdash; is used to compute the correct width to assign to the text box. This width is recomputed and assigned to the text box on every [`input`](https://developer.mozilla.org/en-US/docs/Web/Events/input) event.

- The single &ldquo;ghost&rdquo; element is shared amongst all the &ldquo;autosized&rdquo; text boxes on the page.

__GIF FTW:__

![autoinput-size](/images/autoinput-size/autosize-input.gif)