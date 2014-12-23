---
layout: post
title: "configstore"
date: 2014-03-20 17:53:08 +0530
comments: true
categories: CLI
ogimg: http://nmotw.in/images/configstore/configstore.gif
---

CLI apps normally use configurations for different situations like:

* Saving the state of an app and restoring it.

* Having global and user level configurations for their own benefits.

* Maintaining interval threshold value for cron like activities.

* Storing strings for Internationalization and localization.

And many more similar use cases.


[ConfigStore](https://github.com/yeoman/configstore) is one such node module that helps you to easily load and persist config without having to think about where and how!

This is wonderful module is a gift from [Yeoman](http://yeoman.io) which has about 18432 downloads yesterday alone!

Installing is it just like any other module: `$ npm install configstore`

__API:__

The API set is very simple had has:

* `set(key, val)` -> Set an item.

* `get(key)` -> Get an item.

* `del(key)` -> To delete an item.

* `all` -> Get all the items in the current config store and replace them all with a new object.

* `size` -> Count of the items.

* `path` -> File path to the config store.

__Example usage:__

```javascript

var Configstore =  require('configstore');

var conf = new Configstore('appConf');

/*
  var conf = new ( require('configstore') )('appConf');
  
  var conf = new ( require('configstore') )\
             ('appConf', {'ans': 42});

  i.e  Configstore(id, defaults);
  id -> mandator
  defaults -> optional

*/

// Set some values.
conf.set('life', 42);
conf.set('key', {'scrt': '42'});

// Get some values.
conf.get('life'); // 42
conf.get('key'); // {'scrt': 42}

// Delete a value.
conf.del('life');
conf.get('life'); // undefined.

// Get the count.
conf.size() // 1

// Reset the entier conf with new conf.
conf.all = {'ans' : 42};

```

__Under the covers:__

Config is stored as a [YAML](http://www.yaml.org/) file in `$XDG_CONFIG_HOME` or `~/.config/configstore/your-config.yaml` there is an [issue](https://github.com/yeoman/configstore/issues/10) for JSON support as well.

For the above example:

```sh

$ cat ~/.config/configstore/appConf.yaml

# Would be something like
key:
  scrt: 42
life: 42

```

__GIF FTW!__

![configstore](http://nmotw.in/images/configstore/configstore.gif)
