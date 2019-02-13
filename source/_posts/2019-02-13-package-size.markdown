---
layout: post
title: "package-size"
date: 2019-02-13 00:21:28 +0530
comments: true
categories: util perf cli
---

#[package-size](https://github.com/egoist/package-size)
> Get the bundle size of an npm packages.

`package-size` is a sweet CLI util, that gives us info about the bundle size of npm packages.

__What it does?__

* Install the packages to a temp directory.
* Bundle the packages with webpack and get the bundle size.
* Show you the bundle size and cache it by package version.

__Get it:__ `npm install -g package-size`

__Sample usage:__

```sh
# get the size of vue bundle
package-size vue

# get the size of react+react-dom bundle
package-size react,react-dom

# get the size of vue react+react-dom preact bundles
package-size vue react,react-dom preact

# get the size of react+react-dom without using the cache
package-size react,react-dom --no-cache

# get the size of file in current working directory
package-size ./dist/index.js
# or a package in current working directory, explictly using `--cwd` flag
package-size vue --cwd

# or event multiple versions for the same package!
package-size react@0.10 react@0.14 react@15

# save results to file system in JSON format
# defaults to ./package-size-output.json
package-size cherow --output
# or custom path
package-size cherow --output stats.json

# analyze bundle with webpack-bundle-analyzer
package-size cherow --analyze
```

```js
const getSizes = require('package-size')

getSizes('react,react-dom', options)
  .then(data => {
    console.log(data)
    //=>
    {
      name: 'react,react-dom',
      size: 12023, // in bytes
      minified: 2342,
      gzipped: 534,
      versionedName: 'react@16.0.0,react-dom@16.0.0'
    }
  })
```

__GIF FTW!__

![](/images/package-size/package-size.gif)