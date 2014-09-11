---
layout: post
title: "mongoskin"
date: 2014-07-10 20:09:46 +0530
comments: true
categories: db nosql
---


# mongoskin
> The future layer above node-mongodb-native.

mongoskin -> The promise wrapper for node-mongodb-native, makes life easier by helping us to work easily with mongodb, but how?

Check this out!

Install it like any other module: `$ npm install mongoskin`

With mongoskin you can dburl like `mongodb://localhost:27017/test` or use Replset :

```javascript
var replSet = new ReplSetServers([
        new Server('localhost', 30000),
        new Server('localhost', 30001),
        new Server('localhost', 30002),
]);
```

Where `Server` is `require('mongoskin').Server`


__Example usage of data insertion:__

```javascript
var mongo = require('mongoskin');

db = mongo.db('mongodb://localhost/test');

db.collection('test').insert({foo: 'bar'}, function(err, result) {
    console.log(result);
    db.collection('test').drop();
    db.close();

});

```

It has an extensive [API](https://github.com/kissjs/node-mongoskin#mongoskin-api-part) with sleeker syntax compared with native.

Thanks to [kissjs](http://kissjs.org/) team, specially to [Gui Lin](https://github.com/guileen)
