---
layout: post
title: "time-require"
date: 2014-05-22 22:26:56 +0530
comments: true
categories: performance
ogimg: http://nmotw.in/images/time-require/time-require.gif
---

Were you looking for the stats of how long the require statements took in your scripts?

It's time to use (time-require)[https://www.npmjs.org/package/time-require] a node module that displays the execution time for Node.js modules loading by hooking and tracing all require() calls. 

__Example Usage:__

```sh
$ cat > time-require
require("time-require");
^C

$ node time-require 


Start time: (2014-05-22 16:56:02 UTC) [treshold=1%]
#  module                          time  %
1  text-table (.....ble/index.js)  40ms  ▇▇▇▇▇▇▇▇▇▇▇▇▇▇▇▇ 51%
2  date-time (../...ime/index.js)   5ms  ▇▇ 6%
3  parse-ms (../n...-ms/index.js)  10ms  ▇▇▇▇ 13%
4  pretty-ms (../...-ms/index.js)  12ms  ▇▇▇▇▇ 15%
5  ansi-styles (....si-styles.js)  10ms  ▇▇▇▇ 13%
6  strip-ansi (.....nsi/index.js)   5ms  ▇▇ 6%
7  has-color (../...lor/index.js)   1ms  ▇ 1%
8  chalk (../node...alk/index.js)  20ms  ▇▇▇▇▇▇▇▇ 26%
Total require(): 8
Total time: 78ms
```

This module makes use of a require (hook)[https://github.com/jaguard/time-require/blob/master/src/requireHook.js#L71] which is loaded as the first module so all the other requires gets counted, unhooks and then prints out a neat table with the `totalTime = Date.now() - startTime.getTime();` and the number of modules that were required.

Thanks to the module author [Ciprian Popa](http://jaguard.com)

__GIF FTW!__

![time-require](/images/time-require/time-require.gif)
