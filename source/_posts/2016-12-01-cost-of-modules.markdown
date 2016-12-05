---
layout: post
title: "cost-of-modules"
date: 2016-12-01 13:36:43 +0000
comments: true
categories: cli perf npm yarn
---

#[cost-of-modules](https://www.npmjs.com/package/cost-of-modules)
> Find out which of your dependencies is slowing you down 🐢

`cost-of-modules` is a cheeky module that generates a neat table of dependencies with children and size, which would help us to easily
identify which dependency is slowing the module down.


__Get it:__ `npm install -g cost-of-modules`

_Usage:__ Run `cost-of-modules` in the directory you are working in.

__Options__

`--less`  Show the biggest 10 modules

`--yarn`  Use yarn instead of npm to install dependencies

`--no-install`  Skip installation

`--include-dev`  Include devDependencies as well - for 🚀 collaborator experience


__GIF FTW!__

![cost-of-modules](/images/cost-of-modules/cost-of-modules.gif)
