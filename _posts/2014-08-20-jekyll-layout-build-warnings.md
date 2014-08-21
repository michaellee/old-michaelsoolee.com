---
layout: post
title: "Jekyll Layout Build Warnings"
category: programming
---

Today I installed Jekyll 2.3.0 on my machine. When I ran `jekyll serve --watch` in my _terminal window_ to serve my site locally, I kept seeing this warning for my feed:

> Build Warning: Layout 'none' requested in feed.xml does not exist.

Turns out `layout: none` isn't a valid YAML declaration to designate that the file should render without any particular layout.

The correct way to tell a file to render without a layout is by passing the value null to the _layout_ variable.

```javascript
---
layout: null
---
```