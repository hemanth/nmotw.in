---
layout: post
title: "graphql-request"
date: 2018-02-03 22:46:29 +0530
comments: true
categories: graphql
---

#[graphql-request]()
> Minimal GraphQL client.

`graphql-request` is a minimal GraphQL promise based client. It's perfect for small scripts or simple apps, it doesn't have a built-in cache and has no integrations for frontend frameworks.

__Get it:__ `npm install graphql-request`

__Sample usage:__

```js
import { request, GraphQLClient } from 'graphql-request'

// Run GraphQL queries/mutations using a static function
request(endpoint, query, variables).then(data => console.log(data))

// ... or create a GraphQL client instance to send requests
const client = new GraphQLClient(endpoint, { headers: {} })
client.request(query, variables).then(data => console.log(data))
```

__GIF FTW!__

![graphql-request.gif](/images/graphql-request/graphql-request.gif)
