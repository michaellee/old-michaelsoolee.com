---
layout: post
title: "How to set an anchor tag's target to blank in Markdown converted with Kramdown"
category: work
---

In Markdown, to create a link, you use this syntax:

```
[Google!](http://google.com)
```

Which yields:

```
<a href="http://google.com">Google!</a>
```

What the above does is creates a link that when clicked on, will take you to the linked website in the same browser tab. But sometimes, instead of opening up the website in the same browser tab, you'll want the website to open in its own tab.

You achieve this by applying the `target` attribute like this:

```
<a href="http://google.com" target="_blank">Google!</a>
```

In Kramdown, the converter found in Jekyll allows you to use an [inline attribute list (IAL)](http://kramdown.gettalong.org/syntax.html#inline-attribute-lists). The syntax for this looks like:

```
[Google!](http://google.com){:target='_blank'}
```

IAL is denoted by the use of curly braces followed by a key-value pair.
