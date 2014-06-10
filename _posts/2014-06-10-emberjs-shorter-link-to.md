---
layout: post
title:  "Ember.js' shorter {{link-to}} helper syntax"
categories: ember
---

I feel pretty noobish for just discovering this but there's a way to use Ember's `{{link-to}}` helper as a non-block link. Oh the joys and pains of learning the specifics and various nuances of learning a new language.

The `{{link-to}}` helper is how Ember.js handles links within an application. So for example if you've got a route at `baseurl.com/about`. Instead of using `<a href="/about">About</a>` to render the link, you'd use `{{#link-to 'about'}}About{{/link-to}}`.

Up until now I've been using the `{{link-to}}` tag in its block format. The format which looks like this:

```javascript
/* 
  Opening tag with a # in front of link-to,
  followed by the route and an optional
  object
*/

{{#link-to 'route' object}}

Block of code you're linking

{{/link-to}}

/*
  Followed by a closing tag which is
  denoted by the forward slash before
  the link-to
*/
```

Yesterday, I discovered a shorter syntax which is perfect for simple text links. That syntax looks like this:

```javascript
/*
  So with this syntax you forgo
  the block characters # and /
  and simply write link-to,
  the text for the text link
  and the route you're linking
  to
*/
{{link-to 'Text to link' route}}
```

Much shorter and a lot quicker to write then the block link. I know, you're probably saying, "Well why don't you just let your text-editor autosuggest those things?". I actually do but it's nice to know a languages' nuances.
