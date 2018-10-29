---
layout: post
title: "the-platform"
date: 2018-10-28 15:33:43 +0530
comments: true
categories: react
---

# [the-platform](https://www.npmjs.com/package/the-platform)
> Browser API's turned into React Hooks and Suspense-friendly components.

`the-platform` is a uber fun module that has React Hooks and Suspense friendly componets, it provides the below:


__Hooks:__

```
    useDeviceMotion()
    useDeviceOrientation()
    useGeoPosition()
    useNetworkStatus()
    useMedia()
    useScript()
    useStylesheet()
    useWindowScrollPosition()
    useWindowSize()
```
__Components:__

```
    <Img>
    <Script>
    <Video>
    <Audio>
    <Preload>
    <Stylesheet>
```

P.S: Looks like it's a pun on `#useThePlatform` none the less it's an intresting module.

__Sample usage:__


```js
import { useGeoPosition } from 'the-platform';

const Example = () => {
  const {
    coords: { latitude, longitude },
  } = useGeoPosition();

  // ...
};
```

```js
import React from 'react';
import { Img } from 'the-platform';

function App() {
  return (
    <div>
      <h1>Hello</h1>
      <React.Suspense maxDuration={300} fallback={'loading...'}>
        <Img src="https://source.unsplash.com/random/4000x2000" />
      </React.Suspense>
    </div>
  );
}

export default App;
```

__GIT FTW!__

![](/images/the-platform/the-platform.gif)