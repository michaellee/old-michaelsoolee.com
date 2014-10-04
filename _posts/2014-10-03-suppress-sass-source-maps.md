---
layout: post
title: "Suppress Sass Source Maps When Generating CSS"
category: sass
---

Recently, I updated my Sass gem on my machine and when generating the CSS I noticed an extra file being generated. The file would be named something like `filename.css.map`. I wasn't sure what the file was used for, so doing a quick search, I found that it was used for mapping your CSS file to your Sass files.

This is especially helpful when you've got many Sass partials and you're trying to figure out what CSS came from which Sass file. Sass source map files could then be used in Chrome DevTools to help in your development process. This was a great discovery but there are some instances when I didn't want a sourcemap.

I'm not sure if this was intentional where the source maps are generated automatically or if something is off on my machine. But you can suppress the creation of source maps when generating your CSS. To do so, pass the `--sourcemap=none` option when running the Sass command-line tool.

This is the command that I usually run:

```javascript
sass style.scss:style.css --style compressed --sourcemap=none
```
