---
layout: post
title: "speedline"
date: 2016-05-20 05:01:00 +0000
comments: true
categories: devtool performance
---

#[speedline](https://www.npmjs.com/package/speedline)
>Calculate the speed index and visual performance metrics from chrome dev tool timeline.


[Navigation Timing API](https://developer.mozilla.org/en-US/docs/Web/API/Navigation_timing_API) provides useful data that can be used to measure the performance of a website. 

Unfortunately this API has never been good at capturing the actual *user experience* that's where `speedline` comes to rescue.

It measures **how fast the page content is visually displayed**. 

The current implementation is based on the **Visual Progress from Video Capture** calculation method described on the [Speed Index](https://sites.google.com/a/webpagetest.org/docs/using-webpagetest/metrics/speed-index) page. 

The visual progress is calculated by comparing the distance between the histogram of the current frame and the final frame.


__GET IT:__ 

`$ npm install --global speedline` // For CLI

`$ npm install --save speedline` // As a devdep.

__Sample usage:__

```sh
$ speedline --help

  Usage
    $ speedline <timeline> [options]

  Options
    -p, --pretty  Pretty print the output

  Examples
    $ speedline ./timeline.json
```


__GIF FTW!__ 

![](/images/speedline/speedline.gif)



