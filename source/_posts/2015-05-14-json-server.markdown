---
layout: post
title: "json-server"
date: 2015-05-14 12:53:06 +0000
comments: true
categories: prototyping REST 
---

# [json-server](https://www.npmjs.com/package/json-server)
> REST API with zero coding in less than 30 seconds.

This module by [typicode](https://github.com/typicode) helps front-end developers who need a quick back-end for prototyping and mocking!

__Get it:__ 

Either as a CLI app: `npm install -g json-server`

or as a dep for your script: `npm install --save json-server`

__Sample usage:__

Assume you have a `json.db` like:

```js
{
  "posts": [
    { "id": 1, "title": "json-server", "author": "typicode" }
  ],
  "comments": [
    { "id": 1, "body": "some comment", "postId": 1 }
  ]
}
```

If you are installed module globally, then do a :

```sh
$ json-server json.db

# or

$ json-server http://example.com/file.json
```


if not, include it in your script 

```js
var jsonServer = require('json-server');

var server = jsonServer.create(); // Returns an Express server
var router = jsonServer.router('db.json'); // Returns an Express router

server.use(jsonServer.defaults); // logger, static and cors middlewares
server.use(router); // Mount router on '/'

server.listen(3000);
```


After which the server must be up and running at: `http://localhost:3000`


__Avaliable routes:__

```
GET    /posts
GET    /posts/1
GET    /posts/1/comments
GET    /posts?title=json-server&author=typicode
POST   /posts
PUT    /posts/1
PATCH  /posts/1
DELETE /posts/1

# SLICE
GET /posts?_start=20&_end=30
GET /posts/1/comments?_start=20&_end=30

# SORT
GET /posts?_sort=views&_order=DESC
GET /posts/1/comments?_sort=votes&_order=ASC

# Query
GET /posts?q=internet

# Get the entire DB!
GET /db
```

GET on `/` would look like:

![json-server-screenshot](/images/json-server/json-server.png)


__GIF FTW!__

![json-server](/images/json-server/json-server.gif)

