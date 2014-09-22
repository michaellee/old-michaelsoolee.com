---
layout: post
title: "Oh My ZSH Not Updating"
category: programming
---

I use Oh My ZSH as my terminal shell. From time to time, Oh My ZSH will ask if I want to update it. This morning when I got the prompt and said, "Yes" I want to update it. I immediately got an error that looked like this:


```javascript
[Oh My Zsh] Would you like to check for updates?
Type Y to update oh-my-zsh: y
Upgrading Oh My Zsh


Agreeing to the Xcode/iOS license requires admin privileges, please re-run as root via sudo.


There was an error updating. Try again later?
```

Turns out I was getting this error because the _Command Line Tools_ for OS X were updated on my machine.

To fix this error, I simply had to fire up _Xcode_ and accept the Xcode license. Doing so will require admin privileges. Once I had accepted the license, I ran `upgrade_oh_my_zsh` in Terminal and the upgrade ran without errors.
