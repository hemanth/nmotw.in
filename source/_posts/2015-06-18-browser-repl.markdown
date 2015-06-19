---
layout: post
title: "browser-repl"
date: 2015-06-18 16:46:33 +0000
comments: true
categories: cli 
---

[browser-repl](https://www.npmjs.com/package/browser-repl)
> Launch a repl on your command line to any browser in the cloud.

`browser-repl` is a uber cool module from [automattic](http://automattic.com/) that helps us to get a particular OS/Browser
combo (JS engine) to our CLI with some webdriver protocol, scoket.io and localtunnel magic ;)

Currently supported browsers:

* ie

* ie6

* ie7

* ie8

* ie9

* ie10

* ie11

* opera

* safari

* safari5

* safari6

* safari7

* safari8

* chrome

* chromedev

* firefox

* firefoxdev

* ipad

* ipad4

* ipad5

* ipad5.1

* ipad6

* ipad6.1

* iphone

* iphone4

* iphone5

* iphone5.1

* iphone6

* iphone6.1

* android

* android4.4

* android4.2

* android4.1

__Currently supported platforms:__

* winxp

* win7

* win8

* win8.1

* mac10.6

* mac10.8

* mac10.9

* mac10.10

* linux

* android


__Get it:__

```sh
npm install -g browser-repl
```
__Set up:__


```sh
# In your *.rc file.
export SAUCE_USERNAME="your username"
export SAUCE_ACCESS_KEY="your key"
```

To get the `SAUCE` stuff, sign up for a free OSS account on [SauceLabs](http://saucelabs.com).

__Usage:__

```sh
$ repl

usage: repl <browser>[version] [platform]

options:
 -h: this message
 -k: no remote `console` override
```

__GIF FTW__

![browser-repl](/images/browser-repl/brwoser-repl.gif)



