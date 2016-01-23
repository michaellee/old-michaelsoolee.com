---
layout: post
title: "GitGutter was making my Sublime Text laggy"
category: 'work'
date: 2015-07-30 15:32:00
---

One of the reasons why I like Sublime Text over [other]({{site.url}}/atom-one-dot-ehhh/) [text editors]({{site.url}}/brackets-one-dot-uhhh/) is that it is lightning fast. But recently, I noticed that my Sublime Text was getting a bit laggy. Laggy in the sense that it was slow when I was typing and doing things like finding instances of a given string.

At first I just ignored it and just trudged through it, but today I got fed up with how slow it was. Flipping through the Sublime Text forums, revealed that others had experienced laggy performance as well. I tried a bunch of suggestions but none of them worked except one &mdash; removing GitGutter.

At first, I tried upgrading the GitGutter package and even switching over to it's edge version but it didn't make any improvements. I removed it completely and now Sublime Text is as snappy as it used to be. As much as I enjoyed having what GitGutter had to offer, it wasn't absolutely necessary to my workflow.

I could simply `git diff` in my terminal window to see changes made to any single file.

If you've been experiencing some performance issues with Sublime Text 3 lately, try removing GitGutter.