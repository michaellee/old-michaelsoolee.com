---
layout: post
title: "Updating Rsync on a Mac"
category: 'work'
date: 2015-07-22 09:38:00
---

Rsync is a useful command-line tool to sync files between different locations &mdash; local or remote. By default OSX comes with a version of Rsync but it quite outdated. If you've got Homebrew installed on your machine it makes it super simple to update Rsync.

First I like to run `rsync --version`. This is so I have something to run the Homebrew install against and make sure that the installation worked correctly.

The command to run is `brew install https://raw.githubusercontent.com/Homebrew/homebrew-dupes/master/rsync.rb`. I originally tried running the tap that Homebrew found when running `brew search rsync` but it didn't seem to work correctly.

Once Homebrew finishes installing Rsync, restart your terminal window and you should be good to go. You can run `rsync --version` and you should get a different version number than what you previously saw prior to using Homebrew.