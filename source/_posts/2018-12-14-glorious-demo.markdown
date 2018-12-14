---
layout: post
title: "@glorious/demo"
date: 2018-12-14 23:37:14 +0530
comments: true
categories: css 
---

#[@glorious/demo](https://www.npmjs.com/package/@glorious/demo)
> The easiest way to demonstrate your code in action.

`@glorious/demo` a uniq node module that helps in demonstrating your code in action!

__Get it:__ `npm install @glorious/demo --save`

__Sample usage:__

```js
import '@glorious/demo/gdemo.min.css';
import GDemo from '@glorious/demo';

const demo = new GDemo('#container');
 
const code = `
function greet(){
  console.log("Hello World!");
}
 
greet();
`
 
demo
  .openApp('editor', {minHeight: '350px', windowTitle: 'demo.js'})
  .write(code, {onCompleteDelay: 1500})
  .openApp('terminal', {minHeight: '350px', promptString: '$'})
  .command('node ./demo', {onCompleteDelay: 500})
  .respond('Hello World!')
  .command('')
  .end();
```

P.S: Don't miss to playaround with the [demo](https://glorious.codes/demo?demo=Y29uc3QgZ2RlbW8gPSBuZXcgR0RlbW8oJ1tkYXRhLWRlbW8tY29udGFpbmVyXScpOwoKY29uc3QgY29kZSA9ICdjb25zb2xlLmxvZygibm1vdHcuaW4hIik7JwoKY29uc3QgaGlnaGxpZ2h0ZWRDb2RlID0gUHJpc20uaGlnaGxpZ2h0KAogIGNvZGUsCiAgUHJpc20ubGFuZ3VhZ2VzLmphdmFzY3JpcHQsCiAgJ2phdmFzY3JpcHQnCik7CgpnZGVtbwogIC5vcGVuQXBwKCdlZGl0b3InLCB7IG1pbkhlaWdodDogJzQwMHB4Jywgd2luZG93VGl0bGU6ICdkZW1vLmpzJyB9KQogIC53cml0ZShoaWdobGlnaHRlZENvZGUsIHsgb25Db21wbGV0ZURlbGF5OiAyMDAwIH0pCiAgLm9wZW5BcHAoJ3Rlcm1pbmFsJywgeyBtaW5IZWlnaHQ6ICc0MDBweCcsIHByb21wdFN0cmluZzogJyQnIH0pCiAgLmNvbW1hbmQoJ25vZGUgLi9kZW1vJykKICAucmVzcG9uZCgnbm1vdHcuaW4hJykKICAuY29tbWFuZCgnJykKICAuZW5kKCk7Cg==).

__GIF FTW!__

![@glorious/demo](/images/glorious-demo/glorious-demo.gif)