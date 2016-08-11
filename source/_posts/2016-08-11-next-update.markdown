---
layout: post
title: "next-update"
date: 2016-08-11 13:40:05 +0000
comments: true
categories: npm cli
---

#[next-update](https://www.npmjs.com/package/next-update)
> Can I update the dependencies without breaking the tests?

Summarizing `next-update` from the authors own words:

* A good workflow using *next-update*
    * see available new versions `next-update --available`
    * check latest version of each module using `next-update --latest`
    * install new versions of the desired modules using standard `npm i dependency@version --save`
* You can use custom test command, for example `next-update -t "grunt test"`
    * `npm test` is used by default.
* You can keep each working version in package.json by using `--keep` flag.

__Get it:__ 

`npm install -g next-update  // installs module globally`

`npm install --save-dev next-update`

In your `package.json` :

```js
{
    "scripts": {
        "next-update": "next-update -k true --tldr"
    }
}
```




__Sample usage:__

```js
$ next-update --help | pbcopy
next-update - Tests if module's dependencies can be updated to the newer version without breaking the tests
  version: 1.2.2
  author: {"email":"gleb.bahmutov@gmail.com","name":"Gleb Bahmutov"}

Options:
  --revert           install original module versions listed in package.json   [default: false]
  --available, -a    only query available later versions, do not test them     [default: false]
  --module, -m       checks specific module, can include version name@version  [default: null]
  --latest, -l       only check latest available update                        [default: true]
  --color, -c        color terminal output (if available)                      [default: true]
  --version, -v      show version and exit                                     [default: false]
  --test, -t         custom test command to run instead of npm test          
  --skip             skip running tests first                                  [default: false]
  --all              install all modules at once before testing                [default: false]
  --keep, -k         keep tested version if it is working                      [default: false]
  --allow            allow major / minor / patch updates                       [default: "major"]
  --type             check dependencies of type (all, prod, dev, peer)         [default: "all"]
  --tldr             only print VERY important log messages                    [default: false]
  --changed-log, -L  print commit changes between working versions             [default: true]
```

__GIF FTW:__

![](/images/next-update/next-update.gif)
