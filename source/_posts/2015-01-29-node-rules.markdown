---
layout: post
title: "node-rules"
date: 2015-01-29 17:53
comments: true
categories: engine, rules
---

# [node-rules](https://www.npmjs.com/package/node-rules)
> Business Rules Engine for JavaScript.

`node-rules` is a module of it's own kind, it's a light weight forward chaining Rule Engine!


__Install it:__ `npm install --save node-rules`


__Usage:__

It's a three step process, to get the engine running:

* Defining a Rule.

* Defining a Fact.

* Initialize the rules engine and execute the rule.


__Create a rule:__

```js
/* Sample Rule to block a transaction if its below 500 */
var rule = {
    "condition": function(R) {
        R.when(this.transactionTotal < 500);
    },
    "consequence": function(R) {
        this.result = false;
        this.reason = "The transaction was blocked as it was less than 500";
        R.stop();
    }
};
```

__Create a fact:__

```js
/* Fact with less than 500 as transaction, and this should be blocked */
var fact = {
    "name": "user4",
    "application": "MOB2",
    "transactionTotal": 400,
    "cardType": "Credit Card"
};
```

__Initialize the rules engine:__

```js
/* Creating Rule Engine instance and registering rule */
var R = new RuleEngine();
R.register(rule);
```

__Execute the rule:__

```js
R.execute(fact, function(data) {
    if (data.result) {
        console.log("Valid transaction");
    } else {
        console.log("Blocked Reason:" + data.reason);
    }
});
```

__GIF FTW!__

![](/images/node-rules/node-rules.gif)


Thanks to [Mithun Satheesh](https://twitter.com/mithunsatheesh) for this adventurous module.
