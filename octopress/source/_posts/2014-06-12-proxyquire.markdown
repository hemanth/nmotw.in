---
layout: post
title: "proxyquire"
date: 2014-06-12 09:21
comments: true
categories: test, stub
---

Test cases always involves mocks and stub, sometimes there will be a need to mock `require` itself, that where proxyquire comes for our rescue.

[Proxyquire](http://npmjs.org/package/proxyquire): Proxies nodejs require in order to allow overriding dependencies during testing.

Installing proxyquire: `npm install -D proxyquire`

__Example:__

Say we a file `baz.js` under test and it looks like:

```js

var os = require('os');

module.exports = function() {
	return os.freemem();
}

```

It's evident that the return value of this function will never be a constant value.

How do we test it then?

Have a look at the test case:

```
// Get some assertion helper.
var assert = require('assert');

// First up we require proxyquire
var proxyquire = require('proxyquire');

// We make a mock of what we need.
var osStub = {
	freemem: function() { return 617619456; }
}

// Now some magic ;)
var freemem = proxyquire("./baz",{'os':osStub});

it("should return the amount of free memory", function(){
    assert.equal(freemem(),6176197456);
});
```

That's it! The test case will be green now :)

Proxyquire basically, [replaces](https://github.com/thlorenz/proxyquire/blob/master/lib/proxyquire.js#L135) a module's require function.

There are many other features like:

* 'noCallThru',
* 'callThru',
* 'noPreserveCache',
* 'preserveCache',
* 'load'

Please feel free to go through their extensive API [DOC](https://github.com/thlorenz/proxyquire#api)

__GIF FTW!__

![/images/proxyquire](/images/proxyquire/proxyquire.gif)


Kudos to [Thorsten Lorenz](http://thlorenz.com/about/me) for the wonderful module.

