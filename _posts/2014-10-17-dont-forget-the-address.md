---
layout: post
title: "Don't Forget the Address"
category: html
---

A common practice when architecturing HTML is to wrap a group of elements with an anchor tag. This is so that clicking any of the elements within the anchor tag takes you to a linked page.

An example of this would be creating a button on a page.

```javascript
<a href="http://michaellee.co/subscribe" class="btn btn-primary">
	Click here to Subscribe
	<span class="icon icon-arrow"></span>
</a>
```

One of the benefits of using an anchor tag like this, is that you automatically get a pointer &mdash the little hand with the pointer finger raised &mdash; for the cursor.

Turns out, if you forget the `href` attribute from the anchor tag, you lose the cursor benefit. According to the <a href="http://www.w3.org/html/wg/drafts/html/master/single-page.html#links-created-by-a-and-area-elements" target="_blank">official HTML spec doc for anchor tags</a>:

> The href attribute on a and area elements is not required; when those elements do not have href attributes they do not create hyperlinks.

Although the href attribute is not required, leaving it out does not create a hyperlink thus causing the element to not have the added benefit of the pointer cursor automatically.

So remember, when making a link, don't forget the `href` attribute.
