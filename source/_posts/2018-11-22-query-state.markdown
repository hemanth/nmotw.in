---
layout: post
title: "query-state"
date: 2018-11-22 16:09:44 +0530
comments: true
categories: DOM util
---

#[query-state](https://www.npmjs.com/package/query-state)
> Application state in query string.

`query-state` is a cheeky module that uses `history` API and `encodeURIComponent` magic to maintain the application state in the query string.


__Get it:__ `npm install query-state`

__Sample usage:__

```js

const queryState = require('query-state');

// create a new query state instance
const qs = queryState();

// get current application state from the hash string:
const appState = qs.get();

// you can also monitor for changes in the query string:
qs.onChange(function(appState) {
  // prints new application state on each hash update
  console.log('app state changed!', appState);
});

// If you want to set a new value in the app state:
qs.set('answer', 42);

// Now the query string will have `answer=42` part in it.
console.log(window.location.hash.indexOf('answer=42')) // prints value > 0.

// You can also set multiple values at once:
qs.set({
  name: 'Haddaway',
  song: 'What is love?'
});

// NOTE: The call above merges new properties. It appends two new properties to 
// the current query string

```

__GIF FTW!__

![query-state](/images/query-state/query-state.gif)