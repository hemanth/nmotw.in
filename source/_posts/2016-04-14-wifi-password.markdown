---
layout: post
title: "wifi-password"
date: 2016-04-14 16:15:12 +0000
comments: true
categories: util cli
---

#[wifi-password](https://www.npmjs.com/package/wifi-password)
> Get current wifi password.

Do you remember your wifi password? 

Do you want share it with your guests?

`wifi-password` is the util to use works across OSs.

Basically fires the below commands based on the OS for the given or connected `SSID`:

* `GNU/Linux` -> `sudo cat /etc/NetworkManager/system-connections/${ssid}`;

* `OSX` ->  `security find-generic-password -D AirPort network password -wa ssid`

* `Windows` -> `netsh wlan show profile $(name=${ssid}) $(key=clear)`

__GET IT__:

`npm install --save wifi-password` for API

```js
const wifiPassword = require('wifi-password');

wifiPassword().then(password => {
    console.log(password);
    //=> 'johndoesecretpassword'
});
```


`npm install --global wifi-password` for CLI.

```js
$ wifi-password --help

  Usage
    $ wifi-password
    johndoesecretpassword

    $ wifi-password foo-network
    foosecretpassword
```

__GIF FTW!__

![wifi-password](/images/wifi-password/wifi-password.gif)



