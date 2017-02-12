---
layout: post
title: "common-tags"
date: 2017-02-10 14:24:05 +0000
comments: true
categories: util template es6
---

#[common-tags](https://www.npmjs.com/package/common-tags)
> Common utility template tags for ES2015

🔖 A set of well-tested, commonly used template literal tag functions for use in ES2015+.

🌟 Plus some extra goodies for easily making your own tags.

Provides the below almost self explanatory functions:

* TemplateTag
* codeBlock
* commaLists
* commaListsAnd
* commaListsOr
* html
* inlineArrayTransformer
* inlineLists
* oneLine
* oneLineCommaLists
* oneLineCommaListsAnd
* oneLineCommaListsOr
* oneLineInlineLists
* oneLineTrim
* removeNonPrintingValuesTransformer
* replaceResultTransformer
* replaceSubstitutionTransformer
* safeHtml
* source
* splitStringTransformer
* stripIndent
* stripIndentTransformer
* stripIndents
* trimResultTransformer

__GET IT:__ `npm install --save common-tags`

__Sample usage:__

```js
import {oneLine} from 'common-tags'
 
oneLine`
  foo
  bar
  baz
`)
// "foo bar baz" 
```

__GIF FTW:__

![common-tags](/images/common-tags/common-tags.gif)
