---
layout: post
title: "Responsive Line Breaks in CSS"
category: rwd
external: http://danielmall.com/articles/responsive-line-breaks/
---

One of the common design trends that you see these days are headers with a huge image and text overlayed on top of it. With responsive web design, there's a challenge of breaking the text over several lines to make it look good, while having it look good over a multitude of resolutions.

This is a problem I ran into recently on a project. On desktop, I broke down a line with `<br>`s to make the layout look right. But on smaller screens, the lines just looked hideous. Looking around, I came across [this _Responsive Line Breaks_ solution](http://danielmall.com/articles/responsive-line-breaks/) by Daniel Mall.

It was simple to implement and if you're into OOCSS, you can create a bunch of single-purpose classes at different breakpoints to finetune the layout.
