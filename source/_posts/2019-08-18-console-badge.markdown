---
layout: post
title: "console-badge"
date: 2019-08-18 15:03:48 +0530
comments: true
categories: fun
---

#[console-badge](https://www.npmjs.com/package/console-badge)
> 🎨 Create simple badges in the browser console

`console-badge` fun little less than 1kB util that helps us to console log badges that can be customized and also provides  popular shields.io badge style as the default style.

__Get it:__ `npm install console-badge`

__Sample usage:__


```js
import * as consoleBadge from 'console-badge';

consoleBadge.log({
  mode: 'shields.io',
  leftText: 'console-badge',
  rightText: 'hello world 🚀',
  rightBgColor: '#ffc107',
  rightTextColor: '#1a1a1a'
});

consoleBadge.log({
  leftText: '😎 Check out our code here:',
  leftTextColor: '#000',
  leftBgColor: '#ddd',
  rightText: 'https://nmotw.in',
  rightBgColor: '#000'
});
```

__GIF FTW!__

![console-badge](/images/console-badge/console-badge.gif)
