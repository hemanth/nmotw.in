---
layout: post
title: "isomorphic-fetch"
date: 2015-01-15 20:45
comments: true
categories: util
---

[isomorphic-fetch](https://www.npmjs.com/package/isomorphic-fetch)
> Isomorphic WHATWG Fetch API, for Node & Browserify

`fetch` from GitHub makes it easier to make web requests and handle responses than using an XMLHttpRequest. This polyfill is written as closely as possible to the standard Fetch [specification](https://fetch.spec.whatwg.org).

Well, `fetch` was in the nmotw queue for quite some time now, but this week seems to be special as FF nightly and Chrome canary rolled out this API ;)


__Install it:__  `npm install isomorphic-fetch`

__Sample usage:__

```javascript
// Fetch random XKCD comic.

require('isomorphic-fetch');

fetch('http://xkcd-imgs.herokuapp.com/')
    .then(function(response) {
        return response.json();
    }).then(function(res) {
        console.log(res)
    }).catch(function(ex) {
        console.log('failed', ex)
    });
```

Would log something like:

```
{ url: 'http://imgs.xkcd.com/comics/wikifriends.png',
  title: 'It\'s crazy how much my gut opinion of a movie/song is swayed by what other people say, regardless of how I felt coming out of the theater.' }
```

__GIF FTW!__

![isomorphic-fetch](/images/isomorphic-fetch/isomorphic-fetch.gif)


Thanks to [Matt Andrews](https://mattandre.ws/) for `isomorphic-fetch` (:
