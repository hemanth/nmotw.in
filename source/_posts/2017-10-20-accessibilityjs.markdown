---
layout: post
title: "accessibilityjs"
date: 2017-10-20 13:13:03 +0530
comments: true
categories: a11y
---

#[accessibilityjs](https://www.npmjs.com/package/accessibilityjs)
> Client side accessibility error scanner.

`accessibilityjs` with `0` dependenices does an wonderful job in scaning and reproting accessibility issues for a given page.

It currently can scan and report the bleow problems:

- `ImageWithoutAltAttributeError`
- `ElementWithoutLabelError`
- `LinkWithoutLabelOrRoleError`
- `LabelMissingControlError`
- `InputMissingLabelError`
- `ButtonWithoutLabelError`
- `ARIAAttributeMissingError`

__Get it:__ `npm install accessibilityjs`

__Sample usage:__

```js
import {scanForProblems} from 'accessibilityjs'

function logError(error) {
  error.element.classList.add('accessibility-error')
  error.element.addEventListener('click', function () {
    alert(`${error.name}\n\n${error.message}`)
  }, {once: true})
}

document.addEventListener('DOMContentLoaded', function() {
  scanForProblems(document, logError)
})
```

__GIF FTW!__

![accessibilityjs](/images/accessibilityjs/accessibilityjs.gif)
