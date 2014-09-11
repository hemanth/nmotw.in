---
layout: post
title: "git-promise"
date: 2014-08-14 17:51:17 +0530
comments: true
categories: cli git promise
---

##git-promise

> Simple wrapper that allows you to run any `git` command using a more intuitive syntax.

[git-promise](https://www.npmjs.org/package/git-promise) is a product of a very good combination of `Q` and `ShellJS` and returns a promise for us, it also handles exit code automatically. Parsing the output or dealing with non 0 exit code is also very clean and easy with this.

We can also chain commands, execute the `git` command in a specific dir. If those are not enough it also provides a copule of `util` methods.


Installing it: `$ npm install git-promise`

__Sample usage:__


```javascript
var git = require('git-promise');

git("init")
.then(console.log)
.fail(console.error);
```

That would output something like: `Initialized empty Git repository in ...`

__More complex example:__

Say we have a `test` dir that has a file named `me` with the content `blame me` and we run `git blame` on it.

```javascript
git("blame me", {
    cwd: "blame"
}, function(output, code) {
    // output and cwd will be as specified.
}).then(function(what) {
    // you would have switched back to current dir.
}).fail(function(err) {
    // If there are any errors
}).fin(function() {
    // Finally reach here.
});
```

All in all `git-promise` is a very well composed module and has a lot of potential to get more better, a huge thanks to [Fabio Crisci](https://twitter.com/piuccio) for authoring this module.

__GIF FTW!__

![git-promise](/images/git-promise/git-promise.gif)

