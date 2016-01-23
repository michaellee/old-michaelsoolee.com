---
layout: post
title: "Open Sublime Text from the Mac Terminal"
category: programming
---

Sublime Text, like [MacVim has a useful command line tool]({{site.url}}/launch-macvim-from-terminal/) that allows you to open Sublime Text and files in Sublime Text from the Mac Terminal.

Setting this up is pretty straight forward. Simply enter this command in Terminal:

```javascript
ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl
```

What the command does is create a symlink of the command line tool in your bin folder. The bin folder is where other executable binary files exist.

While creating the symlink, Terminal might complain about not being able to execute the command. If this happens, simply add `sudo` in front of the command and type in your login password.

Now that the tool is installed you can execute commands like these from Terminal:

```javascript
//Opens Sublime Text
subl

//Opens current directory in Sublime Text
subl .

//Opens file in Sublime Text
subl filename
```
