---
layout: post
title: "intl-tel-input"
date: 2018-12-23 11:37:47 +0530
comments: true
categories: DOM
---

#[intl-tel-input](https://www.npmjs.com/package/intl-tel-input)
>International Telephone Input

Eentering and validating international telephone numbers made easy with `intl-tel-input`.

It adds a flag dropdown to any input, detects the user's country, displays a relevant placeholder and provides formatting/validation methods!

__Get it:__ `npm i intl-tel-input`

__Sample usage:__

```html
<input type="tel" id="phone">
```

```js
require("node_modules/intl-tel-input/src/css/intlTelInput.css");
const intlTelInput = require("intl-tel-input");
const input = document.querySelector("#phone");
intlTelInput(input);
```

__GIF FTW!__

![intl-tel-input](/images/intl-tel-input/intl-tel-input.gif)


