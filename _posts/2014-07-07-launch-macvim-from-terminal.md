---
layout: post
title: "Launch MacVim from the Mac OS X Terminal"
categories: programming
---

MacVim is a great complement to Vim for the Mac. One of the reasons why I started using MacVim was its built in support for the yank command to copy to the system's clipboard.

To get a copy of MacVim, you can grab the <a href="https://github.com/b4winckler/macvim/releases" target="_blank">latest snapshot here</a>.

When you download a snapshot of MacVim, you'll find a compressed file that includes MacVim.app, mvim (a command-line tool) and a README file.

One of the great things about using _vim_ is that you can simply type `vim filename.md` to open a file in vim from within the terminal.

Out of the box, MacVim doesn't have support for opening a file from the command-line like _vim_ does, but _mvim_ cli enables us to do the same thing.

## Installation

After installing MacVim by dragging MacVim.app to the _Applications_ folder, open up terminal and navigate to the uncompressed folder that has _mvim_.

Then we're going to move the _mvim_ file to `/usr/local/bin` by typing in this command from the terminal:

`mv mvim /usr/local/bin/`

Now whenever you're in _Terminal_ and want to open a file with _mvim_ simply type:

`mvim filename.md`