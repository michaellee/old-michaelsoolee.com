---
layout: post
title: "A better understanding of how to use Git submodules"
category: "link"
link: "https://chrisjean.com/git-submodules-adding-using-removing-and-updating/"
date: 2015-11-03 23:29:00
---

I've shared about [Git submodules](http://michaellee.co/git-submodules/) before. I recently decided to use submodules again in some projects I'm developing because I decided to fork a Sass library to use and modify for my projects' needs.

Submodules are useful since I can essentially treat a submodule as its own repo and make changes to it separate from the project from which it is used in.

I ran across, Chris Jean's post on git submodules and it definitely gave me a better understanding of Git submodules. If you're interested in using it yourself, I definitely suggest checking out his article.

One thing I would like to add on top of Chris Jean's post is the part on how to remove a submodule.

An extra step that I had to take was to go into the `.git` folder found in my project's root directory. And remove folders found in the `modules` folder to completely remove a submodule.
