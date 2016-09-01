---
layout: post
title: "auto-install"
date: 2016-09-01 14:05:36 +0000
comments: true
categories: cli mad
---

#[auto-install](https://nmp.im/auto-install)
> Auto installs dependencies as you code on save.

Have you ever wished that need to having a tool that would just do an `npm install` of modules that you `import`? 

Well, here is `auto-install` that does exactly what you wished for!


__Get it:__ `npm install -g auto-install`

__Sample usage:__

```sh

# In case you run it in a folder that doesn't have a `package.json`

$ auto-install --help
package.json does not exist
You can create one by using `npm init`

# With a package.json

$ auto-install 
Watchers initialized

```

__CLI Flags:__


`--secure`  Install popular modules only (> 10k downloads in the last month)

`--exact`   Install exact version similar to `npm install express --save-exact`

`--dont-uninstall`   Do not uninstall unused modules

P.S: [Does it protect against typosquatting?](https://github.com/siddharthkp/auto-install/issues/6)


__GIF FTW!__

![auto-install](/images/auto-install/auto-install.gif)
