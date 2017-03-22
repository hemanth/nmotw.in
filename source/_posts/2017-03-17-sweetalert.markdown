---
layout: post
title: "sweetalert"
date: 2017-03-17 11:06:18 +0000
comments: true
categories: dom
---

#[sweetalert](https://www.npmjs.com/package/sweetalert)
>An awesome replacement/alternative for alert().

`sweetalert` is an alternative to annoying alert, it's rather a sweet a simple modal box.

__Get it:__ `npm install --save sweetalert`

__Usage:__

```js
const swal = require('sweetalert');
```

```js
swal("Oops...", "Something went wrong!", "error");
```

```js
swal({
  title: 'Ajax request example',
  text: 'Submit to run ajax request',
  type: 'info',
  showCancelButton: true,
  closeOnConfirm: false,
  disableButtonsOnConfirm: true,
  confirmLoadingButtonColor: '#DD6B55'
}, function(inputValue){
  setTimeout(function() {
    swal('Ajax request finished!');
  }, 2000);
});
```

__GIF FTW!__

![](/images/sweetalert/sweetalert.gif)
