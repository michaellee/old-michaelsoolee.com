---
layout: post
title: "Open Current Directoy in a New Tab in ZSH in the Mac Terminal"
category: programming
---

For my terminal I like to use the shell _ZSH_, specifically [_Oh-My-ZSH_](http://ohmyz.sh/) &mdash; a community-driven, open source configuration of ZSH.

One of the things I do quite often during my workflow is open up additional Terminal tabs. 

For example, I may have one Terminal tab open with Sass watching my .scss files for changes and compiling on the fly as I add new style rules. While that's happening I might want to navigate to a different folder within my project directory without having to stop Sass. It's convenient to simply press `command + t` and get a new Terminal tab starting from the current directory that I was in in the previous tab where Sass is running.

Setting this up is pretty simple. Simply navigate to your .zshrc file.

Once there you'll want to scroll down to the line that says `plugins=()`. I believe by default `git` will automatically be a plugin that's loaded. You'll want to load `osx` and `terminalapp` as well. So your plugins line should look like this once you're done loading those plugins:

```javascript
...
plugins=(git osx terminalapp)
...
```
