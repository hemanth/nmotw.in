---
layout: post
title: "lie-denodify"
date: 2014-04-10 17:38:55 +0530
comments: true
categories: promise 
---

Even though [RSVP](http://nmotw.in/rsvp/) provides a `denodeify` API, [lie-denodify's](https://www.npmjs.org/package/lie-denodify) main focus is to turn a node style callback into a promise based one.

[lie-denofiy](https://www.npmjs.org/package/lie-denodify) internally uses [lie](https://github.com/calvinmetcalf/lie) which is a basic but performanent promise implementation.

All it does to convert an async function to a promise based one is to return a promise with the help of lie:

```javascript
var promise = require('lie');
function denodify(func) {
    return function() {
        var args = Array.prototype.concat.apply([], arguments);
        return promise(function(resolve, reject) {
            args.push(function(err, success) {
                if (err) {
                    reject(err);
                }
                else {
                    resolve(success);
                }
            });
            func.apply(undefined, args);
        });
    };
}
module.exports = denodify;
```

__Installation:__ `npm install lie-denodify`


__Usage example:__


Let's try and covert `fs.stat` function to a promise! 

First of all let's have a look at how `fs.stat` works before conversion.

```js
var fstat = require('fs').stat;

fstat('/tmp',function(err,res){
	if(!err){
	  console.log(res);
	} else {
		throw new Error(err);
	}
});

/*
Would log something like:
{ dev: 16777217,
  mode: 17407,
  nlink: 14,
  uid: 0,
  gid: 0,
  rdev: 0,
  blksize: 4096,
  ino: 144575596,
  size: 476,
  blocks: 0,
  atime: Thu Apr 10 2014 17:38:18 GMT+0530 (IST),
  mtime: Thu Apr 10 2014 17:51:50 GMT+0530 (IST),
  ctime: Thu Apr 10 2014 17:51:50 GMT+0530 (IST) }
 
 And in case of an Error it would throw an error

*/
```

Now, let's convert it into a promise:

```js

var lieDndfy = require('lie-denodify');

var statp = lieDndfy ( require('fs').stat );

statp('/tmp').then(console.log,console.error);

```

__GIF FTW!__

![lie-denodify](/images/lie-denodify/lie-denodify.gif)


Thanks to [Calvin Metcalf](http://calvinmetcalf.com/) the author of lie and lie-denofiy.

Learn to lie this week ;)! 