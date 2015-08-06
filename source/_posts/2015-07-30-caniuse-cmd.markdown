---
layout: post
title: "caniuse-cmd"
date: 2015-07-30 10:32:22 +0000
comments: true
categories: cli util
---

#[caniuse-cmd](https://github.com/sgentle/caniuse-cmd)
> `caniuse.com` on CLI!


`caniuse-cmd` brings the power of [caniuse](http://caniuse.com) on to the command line, it makes use of [caniuse-db](https://www.npmjs.com/package/caniuse-db) module
which provides raw browser/feature support data for the same.


__Install it:__

```sh
npm install --global caniuse-cmd
```

__Sample usage:__

```sh
nmotw> caniuse webrtc --short      
WebRTC Peer-to-peer connections ✔ 55.36% ◒ 0%
  IE ✘  Edge ✘  Firefox ✘ 2+ ✔ 22+ᵖ Chrome ✘ 4+ ✔ 23+ᵖ Safari ✘  Opera ✘ 9+ ✔ 18+ᵖ
  
nmotw> caniuse webrtc --short -a
WebRTC Peer-to-peer connections ✔ 55.36% ◒ 0%
  IE ✘  Edge ✘  Firefox ✘ 2+ ✔ 22+ᵖ Chrome ✘ 4+ ✔ 23+ᵖ Safari ✘  Opera ✘ 9+ ✔ 18+ᵖ                      
  
nmotw> caniuse webrtc --short --abbrv
WebRTC Peer-to-peer connections ✔ 55.36% ◒ 0%
  IE ✘  Edge ✘  Firefox ✘ 2+ ✔ 22+ᵖ Chrome ✘ 4+ ✔ 23+ᵖ Safari ✘  Opera ✘ 9+ ✔ 18+ᵖ                      
  
nmotw> caniuse webrtc --short --abbrev
WebRTC Peer-to-peer connections ✔ 55.36% ◒ 0%
  IE ✘  Edge ✘  FF ✘ 2+ ✔ 22+ᵖ Chr. ✘ 4+ ✔ 23+ᵖ Saf. ✘  Op. ✘ 9+ ✔ 18+ᵖ                                 
  
nmotw> caniuse webrtc --short --abbrev --browser ff
WebRTC Peer-to-peer connections ✔ 55.36% ◒ 0%
                                                                                                        
                                                                                                        
nmotw> caniuse webrtc --long                       
WebRTC Peer-to-peer connections ✔ 55.36% ◒ 0% [W3C Working Draft]
  Method of allowing two users to communicate directly, browser to browser using the RTCPeerConnection API.
  #JSAPI

  IE ✘  
  Edge ✘  
  Firefox ✘ 2+ ✔ 22+ᵖ 
  Chrome ✘ 4+ ✔ 23+ᵖ 
  Safari ✘  
  Opera ✘ 9+ ✔ 18+ᵖ 
```

P.S: Do cehckout the CLI [flags](https://github.com/sgentle/caniuse-cmd#does-it-have-lots-of-command-line-options)

__GIF FTW!__

![caniuse-cmd.gif](/images/caniuse-cmd/caniuse-cmd.gif)

Thanks to [Sam Gentle](https://github.com/sgentle) for bringing this to the CLI.
