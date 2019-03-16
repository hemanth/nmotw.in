---
layout: post
title: "react-window"
date: 2019-03-16 15:14:26 +0530
comments: true
categories: util react
---

#[react-window](https://www.npmjs.com/package/react-window)
> React components for efficiently rendering large lists and tabular data.

From the horse's mouth, what is `react-window`?

> react-window is a complete rewrite of react-virtualized. I didn't try to solve as many problems or support as many use cases. Instead I focused on making the package smaller1 and faster. I also put a lot of thought into making the API (and documentation) as beginner-friendly as possible (with the caveat that windowing is still kind of an advanced use case).

The compoents react-window provides:

* FixedSizeList
* VariableSizeList
* FixedSizeGrid
* VariableSizeGrid

__Get it:__ `npm install react-window`

__Sample usage:__

```js
import { FixedSizeList as List } from 'react-window';
 
const Column = ({ index, style }) => (
  <div style={style}>عمود {index}</div>
);
 
const Example = () => (
  <List
    direction="rtl"
    height={75}
    itemCount={1000}
    itemSize={100}
    layout="horizontal"
    width={300}
  >
    {Column}
  </List>
);
```

__GIF FTW!__

![react-window](/images/react-window/react-window.gif)


P.S: Don't miss to checkout the [demos](https://react-window.now.sh/).