---
layout: post
title: "commitizen"
date: 2018-08-26 14:37:52 +0530
comments: true
categories: cli git 
---

#[commitizen](https://www.npmjs.com/package/commitizen)
> Organized, detailed commits to git.

`commitizen` prompts to fill out any required commit fields at commit time. No more waiting until later for a git commit hook to run and reject your commit or reading the `contribution.md` for the commit format!

__Get it:__ `npm install -g commitizen`

__Set up:__

```sh
$ npm install -g cz-conventional-changelog

$ echo '{ "path": "cz-conventional-changelog" }' > ~/.czrc
```

or

```sh
$ commitizen init cz-conventional-changelog --save-dev --save-exact
```

^ this results in modification of your `package.json` to:

```js
  "config": {
    "commitizen": {
      "path": "cz-conventional-changelog"
    }
  }
```

Now one can just do `git cz` instead of `git commit` and enjoy the benifits!

Also, one could add it to `npm-scripts`

```js
"scripts": {
    "commit": "git-cz"
  }
```

And then execute: `npm run commit`.

__GIT FTW!__

![commitizen](/images/commitizen/commitizen.gif)




```
