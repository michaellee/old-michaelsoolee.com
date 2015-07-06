---
layout: post
title:  "Front-End Architecture"
link: http://nicolasgallagher.com/about-html-semantics-front-end-architecture/#how-i-learned-to-stop-worrying-
categories: programming
response: "Do you write your CSS using BEM or OOCSS? If so care to share resources that helped you learn them?"
---

The way I architect my front-end code has changed dramatically over the past year.

I've started using a CSS naming convention called _BEM_, in which the acronym stands for Block, Element, Modifier. I've also been tangoing with _OOCSS_ principles where there's a separation of structure and skin (or theme). The use of single purpose classes are also very much encouraged in OOCSS.

I must admit, the first time I came across these methodologies, my mind felt like it was about to explode! This is because I literally had to rewire the way I learned how to write CSS.

But once I started to get the hang of it, I found the experience to be a lot more enjoyable and surprised with its overall maintainability.

Trying to advocate these new methodologies to others has been a little tough. I've scoured the Interwebs reading article after article familiarizing myself with the new methods, so I've bought into them over some time. On the other hand having a conversation with someone and trying to get buyin in an hour or two is a challenge.

In case you're reading this and you yourself are exploring _BEM_ and _OOCSS_ I can't recommend enough, checking out Nicolas Gallagher's article on front-end architecture.

The last paragraph especially sums up why I've started to use the two methods.

> When you choose to author HTML and CSS in a way that seeks to reduce the amount of time you spend writing and editing CSS, it involves accepting that you must instead spend more time changing HTML classes on elements if you want to change their styles. This turns out to be fairly practical, both for front-end and back-end developers – anyone can rearrange pre-built “lego blocks”; it turns out that no one can perform CSS-alchemy.

Pre-built lego blocks &ndash; such a powerful imagery.
