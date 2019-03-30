---
layout: post
title: "eshost-cli"
date: 2019-03-30 11:37:02 +0530
comments: true
categories: CLI 
---

#[eshost-cli](https://github.com/bterlson/eshost-cli)
> Run ECMAScript code uniformly across any ECMAScript host.

`eshost-cli` makes it easy to run and compare `ECMAScript` code uniformly across a number of runtimes. Support for runtimes is provided by the library `eshost`.

__Get it:__ `npm install -g eshost-cli`

__Sample usage:__


```sh
nmotw.in> eshost -e 'Date.parse("1 Octopus 2018")'

#### Chakra
NaN

#### JavaScriptCore
1538332200000

#### SpiderMonkey
NaN

#### V8
1538332200000

#### V8 --harmony
1538332200000

#### XS
NaN
```


```sh
nmotw.in> eshost --help
Usage: eshost [options] [input-file]
       eshost [options] -e "input-script"
       eshost --list
       eshost --add [host name] [host type] <host path> --args <host arguments>
       eshost --delete [host name]

Options:
  -e, --eval        eval an expression and print the result
  -x, --execute     execute a multi-statement program
  -h, --host        select hosts by name (glob syntax is supported as well)
  -g, --hostGroup   select host groups by host type
  --tags            select hosts by tag
  -c, --config      select a config file
  --table, -t       output in a table                                  [boolean]
  --coalesce, -s    coalesce like output into a single entry           [boolean]
  --showSource, -i  show input source                                  [boolean]
  --unanimous, -u   If all engines agree, exit(0) with no output, otherwise
                    print and exit(1); implies --coalesce              [boolean]
  --add             add a host
  --edit            edit a host
  --delete          delete a host
  --args            set arguments for a host entry (use with --add)
  --configure-jsvu  Configure jsvu hosts in the config                 [boolean]
  --jsvu-prefix     [OPTIONAL] Set the prefix of the configured hosts. If prefix
                    is "jsvu" then hosts will be configured as, e.g., "jsvu-sm".
                    By default, no prefix (e.g. "sm"). Use this flag with
                    --configure-jsvu.
  --jsvu-root       [OPTIONAL] Use this path containing the .jsvu folder (use
                    this option if .jsvu is located somewhere other than the
                    home directory). Use this flag with --configure-jsvu.
  --help            Show help                                          [boolean]
  -a, --async       wait for realm destruction before reporting results[boolean]

Examples:
  eshost --list
  eshost --add d8 d8 path/to/d8 --args
  "--harmony"
  eshost --add ch ch path/to/ch --tags
  latest
  eshost --add ch ch path/to/ch --tags
  latest,greatest
  eshost --configure-jsvu
  eshost --configure-jsvu --jsvu-prefix
  jsvu
  eshost test.js
  eshost -e "1+1"
  eshost -its -x "for (let i=0; i<10; ++i)
  { print(i) }"
  eshost -h d8 -h chakra test.js
  eshost -h d8,sm test.js
  eshost -g node,ch test.js
  eshost -h d8 -g node test.js
  eshost -h ch-*,node test.js
  eshost -h ch-1.?.? test.js
  eshost --tags latest test.js
  eshost --unanimous test.js
```

__GIT FTW!__

![eshost-cli](/images/eshost-cli/eshost-cli.gif)