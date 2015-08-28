---
layout: post
title: "url-pattern"
date: 2015-08-27 08:37:23 +0000
comments: true
categories: util
---

[url-pattern](https://www.npmjs.com/package/url-pattern)
> easier than regex string matching for urls, domains, filepaths and other strings.

`url-pattern` can capture named parts of strings and conveniently returns them as objects. 

Also does the reverse and generates strings given a pattern and such an object.

__install:__ ``` npm install url-pattern ```

__simple match example:__

```javascript

var UrlPattern = require('url-pattern');

var pattern = new UrlPattern('/api/users/:id');

pattern.match('/api/users/10');
{id: '10'}

pattern.match('/api/products/5');
null
```

__complex match example showing off escaping, wildcards and optional segments:__

```javascript
var pattern = new UrlPattern('(http(s)\\://)(:subdomain.):domain.:tld(/*)')

pattern.match('google.de'); // {domain: 'google', tld: 'de'}

pattern.match('https://www.google.com'); // {subdomain: 'www', domain: 'google', tld: 'com'}

pattern.match('http://mail.google.com/mail'); // {subdomain: 'mail', domain: 'google', tld: 'com', _: 'mail'}

pattern.match('google') ; // null
```

__stringify example:__

```javascript
var pattern = new UrlPattern('/api/users(/:id)');

pattern.stringify() // '/api/users'

pattern.stringify({id: 10})  //' /api/users/10'
```

__GIF FTW!__

![url-pattern](/images/url-pattern/url-pattern.gif)



