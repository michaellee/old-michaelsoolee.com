---
layout: post
title: "Jekyll Layout Build Warnings"
category: programming
---

Today I installed <a href="http://jekyllrb.com/" target="_blank">Jekyll</a> 2.3.0 on my machine. When I ran `jekyll serve --watch` in my terminal to serve my site locally, I kept seeing the warning &mdash; _Build Warning: Layout 'none' requested in feed.xml does not exist._ &mdash; for my feed.

Turns out `layout: none` isn't a valid YAML declaration to designate that the file should render without any particular layout.

The correct way to tell a file to render without a layout is by passing the value null to the _layout_ variable.

```javascript
---
layout: null
---
```
