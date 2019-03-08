---
layout: post
title: "image-promise"
date: 2019-03-08 15:00:54 +0530
comments: true
categories: DOM util
---

#[image-promise](https://www.npmjs.com/package/image-promise)
> Promisfied image loading! 

Load one or more images, return a promise that resolves if the image loads or rejects in case of an error.

__Get it:__ `npm install image-pormise`

__Sample code:__

```js
var images = ['cat.jpg', 'dog.jpg'];
// var images = $('img'); // it can also be a jQuery object
// var images = document.querySelectorAll('img'); // or a NodeList

loadImage(images)
.then(function (allImgs) {
	console.log(allImgs.length, 'images loaded!', allImgs);
})
.catch(function (err) {
	console.error('One or more images have failed to load :(');
	console.error(err.errored);
	console.info('But these loaded fine:');
	console.info(err.loaded);
});
```

```
const images = [
  "https://unsplash.it/800/600?random&0",
  "https://unsplash.it/800/600?random&1",
  "https://unsplash.it/800/600?random&2",
  "https://unsplash.it/800/600?random&3"
];

(async () => {
    try {
        const imgs = await ImageLoader(images);
    } catch(err) {
        console.error(err.errored);
    }
})();

```

```
// for CORS enabled imgs
const image = 'http://catpics.com/cat.jpg';

loadImage(image, { crossorigin: 'anonymous' })
.then(function (img) {
	ctx.drawImage(img, 0, 0, 10, 10);

	// now you can do this
	canvas.toDataURL('image/png')
})
.catch(function () {
	console.error('Image failed to load :(');
});
```

__GIF FTW!__

![image-promise](/images/image-promise/image-promise.gif)