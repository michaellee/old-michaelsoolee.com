---
layout: post
title: "Speed up Ruby gem install"
category: programming
---

Ruby gems are awesome! But some gems take forever to install. To help speed things up, you can install the gem without including the docs. The speed gain isn't insanely significant but it helps.

If you want to exclude the docs on a single gem install, you can type this in after your `gem install gemname` command:

```javascript
gem install jekyll --no-ri --no-rdoc
```

In the example above, I'm trying to install the gem for [Jekyll](http://jekyllrb.com/). By adding `--no-ri --no-rdoc` options the docs won't be included with the install.

But, typing in `--no-ri --no-rdoc` after every gem install command is tedious you say? You can make it more permenant so that every time you use `gem install` the document will be excluded automatically.

To do this navigate to the `~/.gemrc` file. Then add this line:

```javascript
gem: --no-document
```
