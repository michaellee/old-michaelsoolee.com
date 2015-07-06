---
layout: post
title: "Sass Source Maps and Google DevTools"
category: sass
link: "https://developer.chrome.com/devtools/docs/css-preprocessors"
---

Yesterday, I noticed that when I [compiled my Sass files, it would output an extra file; called a source map](http://michaellee.co/suppress-sass-source-maps/). Turns out this file is used to map the compiled CSS back to the corresponding Sass source files. This is useful in scenarios when you've got a lot of different folders and partials. I then discovered, you could use this source map file in Google DevTools. This made me happy and has helped me save time from searching through files in my project.
