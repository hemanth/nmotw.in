---
layout: post
title: "jsonselect"
date: 2014-09-04 18:20:10 +0530
comments: true
categories: util
ogimg: http://nmotw.in/images/jsonselect/jsonselect.gif
---

JSONSelect defines a language very similar in syntax and structure to
[CSS3 Selectors](http://www.w3.org/TR/css3-selectors/). 

JSONSelect expressions are patterns which can be matched against JSON documents.


Installing it: `npm install jsonselect`


__Sample usage:__


```javascript
var select = require('jsonselect');

select(user,{only: '.friends'});

/*
{ friends: 
   [ { username: 'bob', password: 'bob pass' },
     { username: 'joe', password: 'joe pass' },
     { username: 'jeff', password: 'jeff pass' } ] }
*/

select(user,{only: '.friends', except: '.password'});

/*
{ friends: 
   [ { username: 'bob' },
     { username: 'joe' },
     { username: 'jeff' } ] }
*/

```

P.S: This module is still in the beta phase. Do checkout [jsonselect.org](http://jsonselect.org/#overview)


__GIF FTW!__

![jsonselect](/images/jsonselect/jsonselect.gif)


Thanks to [Lloyd Hilaiel](http://lloyd.io/) and wish me the very best with this module!