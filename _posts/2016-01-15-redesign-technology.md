---
layout: post
title: "Site redesign: Technology Choices"
category: work
---

This is the last post in my recent series on my site's redesign. In this post, I intend to share the technology choices I made for the new site redesign. If you're interested you could read about [my decisions on layout]({{site.url}}/redesign-layout) and [typography for the redesign]({{site.url}}/redesign-typography).

## Content Management System or lack thereof

For almost 3 years now, this site has been built exclusively with Jekyll. Jekyll is a static-site generator, that does away with databases and any dynamic software in favor of static files. What this means is, I can write my blog posts in markdown, type a few commands in my terminal and Jekyll will generate a website for me with just HTML, CSS and JavaScript. I then type in a few more commands in my terminal and those files go straight to my server.

Now you might be thinking, that's all fine and dandy, but what's so great about static files and no databases? My response would be, "No worries :)". What I mean by this is, since I don't have to worry about any databases or software running my site, I don't have to worry about updates, viruses or ever losing my data. I can simply focus on designing a great experience for my audience and writing great content.

My entire site, is [versioned on GitHub](https://github.com/michaellee/michaelsoolee.com) and weighs-in less than 5 MB. Because it is versioned, I don't ever have to worry about losing years worth of writings. Another benefit in building my site in Jekyll, the resources needed to run the site are very little. This site is running on a [VPS at DigitalOcean](https://m.do.co/c/af0ae1cd97ec) and all it needs is an nginx server. Since there is no querying a database, this makes the site snappy and fast.

If you've never heard of or used [Jekyll](http://jekyllrb.com), I can't recommend it enough. I love it so much, I'm writing [a book on how to build websites with Jekyll]({{site.url}}/jekyll-field-guide).

## CSS Library

I've never enjoyed building sites with CSS libraries like Foundation or Bootstrap. I always thought they were overkill and too much overhead to learn to be productive. A few years back, I stumbled upon modular CSS and fell in love with it. The library that I use is based off of modular CSS and it is called, [Basscss](http://www.basscss.com) by Brent Jackson. I've been following Brent's work for some time and have been impressed with his other projects.

When Brent released, Basscss, I was sold on it. CSS has a lot of bad rap with developers. Most of the time, the heat comes from the fact that CSS could get a bit out of hand and thus making it unwieldy to manage. Not to mention, class names that often times have no meaning whatsoever.

With a library like Basscss, each class name is concise and easy to memorize. The classes are often single purpose in nature so it makes them easy to combine without any unintentional side effects. You can look at an element, see what classes have been applied to it and almost immediately know what it is doing, without having to track down its corresponding style declaration in a stylesheet.

Let me give you an example.

```
<a href="#" class="btn btn-primary bg-red px2">Click me</a>
```

The above link element has `.btn` and `.btn-primary` declared. Immediately, I know that some button-like visual properties were applied from the library. Properties like rounded corners, slightly bolded text and a hover and active state. From there I know that the button is red because of `.bg-red`. In Basscss, all colors that start with the `.bg-` prefix applies the corresponding color to the `background-color` property. Finally, `.px2` tells me that there is a padding of 1rem applied along the x-axis meaning the left and right. Since `p` stands for padding, `x` in the context of padding means padding-left and padding-right and `2` is 2 * 0.5rem.

## Hosting

Ever since I became a devout user of Jekyll, I've hosted the site on [GitHub Pages](https://pages.github.com). Pages makes it super easy to deploy static sites, with your own custom domain and on their servers, completely free. If you already have your site's codebase on GitHub, Pages might be a good option for you.

Simply doing a `git push` would not only save my updates to GitHub and it those changes were almost immediately reflected on the site. Super easy and convenient.

Currently, my site isn't hosted on GitHub Pages anymore. It is hosted on a [VPS from DigitalOcean](https://m.do.co/c/af0ae1cd97ec). Although I don't have the convenience of GitHub Pages and I had to learn a lot about server setup to get the VPS up and running for my site, I'm gaining the ability to serve my site over SSL on a custom domain. I haven't implemented SSL yet on the site, but it is something I plan on doing in the future.

Since I've used DigitalOcean in the past, the interface was familiar and I had some left over credit to run the server for a few months completely free. Otherwise, paying $5 a month for a VPS is cheap.

## Conclusion

This post concludes my series on covering my site's redesign. I'm sure there are some other tech considerations that went into this site that I'm not covering but what I've shared above covers the bulk of what keeps this site ticking. If you have any questions on anything, feel free to let me know and I'd love to share what I can.

As far as when the new site will be posted, I'm hoping before the end of the month. Thanks for following along.
