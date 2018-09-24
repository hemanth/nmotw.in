---
layout: post
title: "please-upgrade-node"
date: 2018-09-23 15:42:17 +0530
comments: true
categories: cli
---

#[please-upgrade-node](https://www.npmjs.com/package/please-upgrade-node)
> 💁 show a message to your users to upgrade Node instead of a stacktrace

`please-upgrade-node`checks if the users node version is statisfying the `engines` version in your `package.json` if not warns, uber useful for CLI apps relying on versions.

__GET IT:__ `npm install please-upgrade-node`

__Sample usage:__


```js
#!/usr/bin/env node
const pkg = require('./package.json')
require('please-upgrade-node')(pkg) // <- Must run BEFORE requiring any other modules
```

in `package.json`:

```
{
  "engines": {
    "node": ">=6"
  }
}
```

P.S: `>=` is the only operator supported.

You could also:

```js
pleaseUpgradeNode(pkg, {
  exitCode: 0, // Default: 1
  message: function(requiredVersion) {
    return 'Oops this program require Node ' +  requiredVersion
  }
})
```

__GIF FTW!__

![please-upgrade-node](/images/please-upgrade-node/please-upgrade-node.gif)
