---
layout: post
title: "Font Icon Not Rendering, Check text-transform"
category: programming
---

At NC State, we use a font-icon set where letters are assigned to the `content` property in the `:after` psuedo selector. In one instance when I was trying to call a font-icon in an HTML element, I noticed the icon wasn't rendering.

Looking at the console, my team and I discovered an [issue with font-icon files being served from other subdomains](http://schock.net/articles/2013/07/03/hosting-web-fonts-on-a-cdn-youre-going-to-need-some-cors/). We were able to mitigate this by changing the CORS settings on our server.

After fixing the server issue, I still noticed that the font-icon wasn't rendering.

One of the other devs pointed out that the `content` property of the icon I was trying to use was applied to a lowercase letter. Checking all the styles on the element, we noticed that it had a `text-transform` of uppercase. Which to my surprise also made the `content` for the pseudo selector, uppercase.

Applying a `text-transform: lowercase` to that element seemed to fix the problem.
