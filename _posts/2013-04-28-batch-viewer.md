---
layout: post
title:  "Batch Viewer"
date:   2013-04-28 22:21:03
categories: projects
---

I am thankful for Adam Whitcroft's <a href="http://adamwhitcroft.com/batch/" title="Adam Whitcroft's Batch icons" target="_blank">Batch interface icons</a>. Batch is my go to set of icons for most of my design work these days.

Batch is a 300+ and growing, free library of icons that Adam has given to the world. And through his giving, I and I believe many others have benefitted from his generosity.

While using Batch, I realized I search for icons in one of two ways.

The first way I usually search for an icon is visually. Visually I know what kind of icon I'm going for, so I'll navigate to my Batch folder and then hit spacebar over the first icon at the top of the folder and scroll down as I scan through the icons in Quick Look until I find the one I'm looking for.

Not the most efficient way, I know. Since I don't know where an icon usually is in the bunch, the search and find process can be really short or long based on the icon's position.

The second way I search for an icon is by name. Usually if I've used the icon enough times I will remember what it's called so I can go straight to the icon based on a name. But occasionally, I'll think an icon has a specific name but will end up being named something completely else.

When the name is completely different from what I thought it was called, then I end up using my first method of scanning for an icon. Which could end up being a long ordeal.

I always thought it'd be neat if a simple web page existed where I can quickly scan for an icon visually by scrolling but also be able to quickly search for keywords in a name if I wasn't quite sure of the full filename.

So one day I built one during a couple of hours where I felt the need to simply create something.

The web page was built using Sinatra. With Ruby's Dir class, I was able to upload the files to a folder and read all the file names from there. Then using the file name, generate the icon and the filename as a title, together.

Like I said the site was made in a couple of hours so it's very simple. Hopefully it makes scanning and finding icons a little bit quicker.

If you'd like to see how it was built, you can <a href="https://github.com/michaellee/batch-viewer" title="Batch Viewer on Github" target="_blank">find it on Github</a>. If you think you can make it better, than by all means, do it! Fork the project, make some improvements and send a pull request.

Finally, if you find Adam Whitcroft's Batch icons to be helpful then please let him know! It's projects like these that benefit so many people. Thanks Adam!
