---
layout: post
title: "music meta data"
date: 2014-06-05 18:08:35 +0530
comments: true
categories: meta
ogimg: http://nmotw.in/images/music-meta-data/mmd.gif
---

[musicmetadata](https://github.com/leetreveil/musicmetadata) is a streaming music metadata parser for node and the browser, but out focus is more on node side here.

It's worth noting that this module is influnced by [node-id3](https://github.com/aadsm/node-id3)

This module makes it easier to extra meta data from a given audio file, it supports:

* mp{1.1, 2.2, 2.3, 2.4, 3}
* m4a, mp4.
* vorbis (ogg, flac)
* asf (wma, wmv)

It parses the files for meaning fully meta data, for example it maintaines a common list of [GENRES](https://github.com/leetreveil/musicmetadata/blob/master/lib/common.js#L212) and [pic types](https://github.com/leetreveil/musicmetadata/blob/master/lib/common.js#L188) that will be matched and extracted from the Meta Data Atom. 

But the clean part of this module is it makes use of Streams :-)

Kudos to [Lee Treveil](http://twitter.com/leetreveil) on this.

__Let's see an example:__

```
var fs = require('fs');
var mmd = require('musicmetadata');

var parser = mmd( fs.createReadStream('FreeSWSong.ogg') );

parser.on('metadata',function(res) {
    console.log(res);
});

```

This would log something like:

```sh
{ title: 'Free Software Song',
  artist: [ 'Mark Forry, Yvette Osborne, Ron Fox, Steve Finney, Bill Cope, Kip McAtee, Ernie Provencher, Dan Auvil' ],
  albumartist: [],
  album: '',
  year: '2009',
  track: { no: 0, of: 0 },
  genre: [ 'Ethnic' ],
  disk: { no: 0, of: 0 },
  picture: [],
  duration: 0 }
```

 Now, we could also listen for an event for a particular entinty of the meta data or custom metadata types that are not part of the standard metadata.

```js

parser.on('artist', function(res){
	console.log(res);
});

```

Would log something like : `[ 'Mark Forry, Yvette Osborne, Ron Fox, Steve Finney, Bill Cope, Kip McAtee, Ernie Provencher, Dan Auvil' ]`

A `done` event is triggered once the parsing is done, we could as well listen for it, to detect any errors.

__GIF FTW!__

![music-meta-data](/images/music-meta-data/mmd.gif)
