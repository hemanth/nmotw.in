---
layout: post
title: "carbon-now-cli"
date: 2019-03-22 22:28:38 +0530
comments: true
categories: 
---

#[carbon-now-cli]()
> carbon code images from CLI.

`carbon-now-cli` is a CLI interface for 🎨 Beautiful images of your code — from right inside your terminal!

__It also porivdes the below functionality:__

- 🖼 Downloads the **real**, **high-quality** image (*no DOM screenshots*)
- ✨ Detects file type **automatically**
- 🗂 Supports **all** file extensions supported by [carbon.now.sh](https://carbon.now.sh) and [more](https://github.com/mixn/carbon-now-cli/blob/master/src/helpers/language-map.json)
- ⚡️ Interactive mode via `--interactive`
- 🎒 Presets : save and reuse your favorite settings
- 🖱 Selective highlighting `--start` and `--end`
- 📎 Copies image to clipboard via `--copy` (**cross-OS** 😱)
- 📚 Accepts file, `stdin` or clipboard content as input.
- 🐶 Displays image directly in supported terminals
- ⏱ Reports each step and therefore *shortens the wait*
- 👀 Saves to given location or only opens in browser for manual finish.
- 🌈 Supports saving as `.png` or `.svg` — just like Carbon
- 📏 Supports `2x`, `4x` or `1x` resolutions — just like Carbon
- ✅ Tested
- ⛏ Maintained

__Get it:__ `npm i -g carbon-now-cli`


__Sample usage:__

```sh
$ carbon-now --help

Beautiful images of your code — from right inside your terminal.

Usage
  $ carbon-now <file>
  $ pbpaste | carbon-now
  $ carbon-now --from-clipboard

Options
  -s, --start          Starting line of <file>
  -e, --end            Ending line of <file>
  -i, --interactive    Interactive mode
  -l, --location       Image save location, default: cwd
  -t, --target         Image name, default: original-hash.{png|svg}
  -o, --open           Open in browser instead of saving
  -c, --copy           Copy image to clipboard
  -p, --preset         Use a saved preset
  -h, --headless       Use only non-experimental Puppeteer features
  --config             Use a different, local config (read-only)
  --from-clipboard     Read input from clipboard instead of file
```

__GIF FTW__

![carbon-now-cli](/images/carbon-now-cli/carbon-now-cli.gif)
