---
layout: post
title: "portscanner"
date: 2017-12-17 09:46:40 +0000
comments: true
categories: cli
---

#[portscanner](https://www.npmjs.com/package/portscanner)
> port scanner!

`portscanner` helps us to check the port status and free port for a given host.

__Get it:__ `npm install portscanner`

__Sample usage:__


```js

const portScanner = require('portscanner');

portscanner.checkPortStatus(3000, '127.0.0.1')
.then(console.log);

portscanner.findAPortInUse([3000, 3005, 3006], '127.0.0.1')
.then(console.log)
.catch(console.error);
```

__GIF FTW__

![portscanner.gif](/images/portscanner/portscanner.gif)

