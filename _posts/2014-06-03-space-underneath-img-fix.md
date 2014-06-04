---
layout: post
title:  "Space Underneath <img> Fix"
categories: css
---

Recently while working on <a href="http://www.edisonunion.com/" target="_blank">Edison Union's</a> shop view, I noticed that there was some odd spacing underneath product images.

![](https://dl.dropboxusercontent.com/u/1228961/michaellee/2014/06%20-%20June/img-space-01.png)

See it? No? Maybe this helps.

![](https://dl.dropboxusercontent.com/u/1228961/michaellee/2014/06%20-%20June/img-space-02.png)

See it now? It's throwing off my layout and the title doesn't look centered. I inspected all the elements around the image and didn't notice any margin that might have caused the spacing issue.

Doing a <a href="http://stackoverflow.com/a/6584455/703220" target="_blank">quick search</a> I learned that `<img>` tags are considered to be `inline` elements. The weird space was caused by space reserved for descenders in letters like `g` and `p`.

![](https://dl.dropboxusercontent.com/u/1228961/michaellee/2014/06%20-%20June/img-space-03.png)

To fix this, simply apply a style of `display: block;` to the <img> element.

![](https://dl.dropboxusercontent.com/u/1228961/michaellee/2014/06%20-%20June/img-space-04.png)

This gets rid of the odd spacing underneath the <img> element, resulting in something like the image below.

![](https://dl.dropboxusercontent.com/u/1228961/michaellee/2014/06%20-%20June/img-space-05.png)

Much better! Here's also an example of the <a href="http://codepen.io/michaellee/pen/mILEK">solution on CodePen</a>.

<p data-height="268" data-theme-id="0" data-slug-hash="mILEK" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/michaellee/pen/mILEK/'>Extra Space Beneath <img> Fix</a> by Michael Lee (<a href='http://codepen.io/michaellee'>@michaellee</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>
