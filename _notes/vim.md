---
layout: note 
title: Vim 
lastupdated: 2015-10-27  
---

## Navigating

These should be performed in *command mode*.

`h` Move to the left

`l` Move to the right

`j` Move down 

`k` Move up 

## Editing

`>>` Indent line by shiftwidth spaces. shiftwidth is defined in a .vimrc file.

`[1-9]>>` Indents line by shiftwidth spaces starting from the line your cursor is currently on. So if I did `3>>` this would shift the current line plus the 2 followng lines

`s` Delete and enter insert mode. Like `x` you'll want the cursor over the character you want to replace.

## Tips

### Refresh changes to a currently open file

`:edit` using this command without specifying a file name will reload the current file.

### Refresh directory changes in NERDTree

If you work with a project that has multiple contributors, you know that files and folders in your project directory could change constantly. If you're a user of NERDTree simply hitting the `r` key will refresh your project in NERDTree
