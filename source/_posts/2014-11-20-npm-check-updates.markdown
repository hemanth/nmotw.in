---
layout: post
title: "npm-check-updates"
date: 2014-11-20 19:46:00 +0530
comments: true
categories: CLI util
---

# [npm-check-updates](https://www.npmjs.org/package/npm-check-updates)

Finding all updates to dependencies and updating them is very easy with `npm-check-updates`.

__Install it globally:__ `npm install -g npm-check-updates`
 
__Sample usage:__

```sh
$ npm-check-updates 
npm http GET http://registry.npmjs.org/read-chunk
npm http GET http://registry.npmjs.org/mocha
npm http GET http://registry.npmjs.org/browserify
npm http 304 http://registry.npmjs.org/browserify
npm http 304 http://registry.npmjs.org/read-chunk
npm http 304 http://registry.npmjs.org/mocha

"browserify" can be updated from ^3.0.0 to ^6.3.2 (Installed: 3.44.2, Latest: 6.3.2)
"read-chunk" can be updated from ^0.1.0 to ^1.0.0 (Installed: 0.1.0, Latest: 1.0.0)
```
```sh
$ npm-check-updates -u

"browserify" can be updated from ^3.0.0 to ^6.3.2 (Installed: 3.44.2, Latest: 6.3.2)
"read-chunk" can be updated from ^0.1.0 to ^1.0.0 (Installed: 0.1.0, Latest: 1.0.0)

package.json upgraded

$ npm-check-updates 

All dependencies match the latest package versions :)

```

__GIF FTW!__

![](/images/npm-check-updates/npm-check-updates.gif)

Thanks to Tomas Junnonen for this cute little util.