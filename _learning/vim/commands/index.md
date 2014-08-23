---
layout: post
title: "Vim: Commands"
---

I grew up playing Street Fighter 2 as a kid. What made Street Fighter 2 so great was that you could combine a string of moves and your character will perform a special attack.

When I started learning Vim and more specifically commands, I thought of commands as special attacks for Vim. This was because Vim commands are composed of other commands. 

What this means is that Vim has single action commands such as `y` which is for yanking or Vim's equivalent of the copy command. But you can chain multiple commands to execute a bigger command.

So going back to the `y` command, you can do a combination like `ggyG`. What this command does is goes to the top of your document to the very first character, which was defined by `gg`. Then it starts a yanks to a position you tell Vim. In this case it will be the last line and the last character since we used the `G` command.

This page serves as a list of commands (special Vim attacks) I've found helpful.

## Copy all lines of document
`ggyG` 
