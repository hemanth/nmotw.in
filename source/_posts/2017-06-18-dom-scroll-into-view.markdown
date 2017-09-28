---
layout: post
title: "dom-scroll-into-view"
date: 2017-06-18 15:32:27 +0530
comments: true
categories: dom 
---

#[dom-scroll-into-view](https://www.npmjs.com/package/dom-scroll-into-view)
> scroll node in contain to make node visible

`dom-scroll-into-view` a dom util that helps in scrolling to node that is targeted. 

__Get it:__ `npm install dom-scroll-into-view`

__Sample usage:__

```js
var scrollIntoView = require('dom-scroll-into-view');
scrollIntoView(source,container,config);
```

```js
//config
   { 
       alignWithLeft,
       alignWithTop,
       allowHorizontalScroll,
       onlyScrollIfNeeded,
       offsetTop,
       offsetLeft,
       offsetBottom,
       offsetRight
   }
```

__GIF FTW!__

![dom-scroll-into-view.gif](/images/dom-scroll-into-view/dom-scroll-into-view.gif)