---
layout: post
title: "Update rbenv's ruby-build List"
category: rbenv ruby
---

On my machine, I use [rbenv to manage my Ruby environment](https://github.com/sstephenson/rbenv). Occasionally, the required Ruby version for a project that I'm working on will be higher than what I have set up on my machine.

This results in having to upgrade my Ruby version. In order to do this, rbenv &mdash; specifically rbenv's ruby-build plugin &mdhash; will have to have the list of the latest Ruby versions before being able to download and set that up on your machine.

To update ruby-build simply `cd` into the folder with `cd ~/.rbenv/plugins/ruby-build` and pull the latest version by running `git pull`.

Once the pull request is complete, you should be able to run `rbenv install -l` and see a list of the latest Ruby versions available for you to install.
