---
layout: post
title: "json-schema-faker"
date: 2017-03-10 12:19:12 +0000
comments: true
categories: mock jsonschema 
---

#[json-schema-faker]()
> JSON-Schema + fake data generators

Use [JSON Schema](http://json-schema.org/) along with fake generators to provide consistent and meaningful fake data.


__Get it:__ `npm install --save json-schema-faker`

__Sample usage:__


```js

const jsf = require('json-schema-faker');

const schema = {
  "type": "object",
  "properties": {
    "name": {
      "type": "string",
      "faker": "name.findName"
    },
    "email": {
      "type": "string",
      "faker": "internet.email"
    }
  },
  "required": [
    "name",
    "email"
  ]
};


console.log(jsf(schema));


/*

^ Would log something like:

{
  "name": "Annetta Weimann",
  "email": "Assunta_Beer@gmail.com"
}
*/
```

__GIF FTW!__

![json-schema-faker](/images/json-schema-faker/json-schema-faker.gif)


P.S: Don't forget to checkout their web-[app](http://json-schema-faker.js.org/)!
