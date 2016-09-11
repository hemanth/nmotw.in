---
layout: post
title: "node-wifi-scanner"
date: 2016-08-18 11:33:58 +0000
comments: true
categories: wifi util security 
---

#[node-wifi-scanner](https://www.npmjs.com/package/node-wifi-scanner)
> Scans the available WiFi networks.

`node-wifi-scanner` scans the available WiFi networks across operating systems and returns an array with objects, each object representing a network with the following properties:

* channel: WiFi channel

* ssid: SSID of the network (if available)

* mac: MAC Address of the network access point

* rssi: signal strength


__Get it:__ `npm install --save node-wifi-scanner`

__Sample usage:__

```js
const scanner = require('node-wifi-scanner');

scanner.scan((err, networks) => {
  if (err) {
    console.error(err);
    return;
  }
  console.log(networks);
});
```

Would log something like:

```sh
[ { ssid: 'Micromax A106',
    mac: '82:6a:b0:b7:fe:d2',
    channel: 6,
    rssi: -85 } ]
```

Basically uses the underlying OS tools to do the task:

* airport on Mac OS-X: `airport -s`

* netsh on Windows: `netsh wlan show networks mode=Bssid`

* iwlist on Linux: `iwlist scan`

__Features that would be nice to have:__

* Promises rather than callbacks.

* allowing users to select the network and login in from CLI.

* Look for a better name, rather that `node-wifi-scanner` ?

__GIF FTW!__

![node-wifi-scanner](/images/node-wifi-scanner/node-wifi-scanner.gif)

