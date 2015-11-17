---
layout: post
title: "Brackets 1.uhhh"
category: 'work'
date: 2015-07-14 10:35:00
---

So yesterday afternoon, a friend of mine mentioned that he had read my [short review on Atom](http://michaellee.co/atom-one-dot-ehhh/) and was curious if I could take Brackets by Adobe for a spin. I thought sure why not. I was midway into my work day so I decided to download Brackets and force myself to use it for the rest of the day. In short, it was painful.

<!--more-->

To recap, my indicator whether an editor will work for me or not is simply, does it give me a workflow boost and can I get work done. As long as that criteria is fulfilled, I dig the editor.

After my work day was over yesterday, it just wasn't looking too good for Brackets. So I decided to sleep on it and try again this morning. Did it get any better? Let's just say I kept scratching my head and didn't get much work done. So I'm taking a pause to write this post and then switching back to Sublime Text.

Here is a list of my pros and cons for Brackets.

## Pros

- Installing the CLI isn't automatic (something Atom seems to do automatically) but it is super easy to install (something that is quite manual in Sublime Text). Simply click *File > Install Command Line Shortcut*. Which will give you the ability to open brackets from the command line.
- It seems pretty fast. At least faster than Atom from what I can see.
- Pretty nice plugins. I think this credits to the individual developers maintaining the plugin projects and not so much Brackets. One plugin I installed and thought was quite awesome was [Brackets git](https://github.com/zaggino/brackets-git). Which gives you a pretty good integration with Git as well as things like change indicators in the document's gutter.

## Cons

- There is no preferences window. Awkwardly it is found under a menu called debug
- Weird key combinations &mdash; a shortcut I use often is the quick open command to quickly open a file within a project directory. In Atom and Sublime it is `command + t`, in Brackets `command + shift + o`. Learning this combination would take quite a bit of time I imagine since I've built muscle memory in my left hand to handle a lot of the shortcuts. In Brackets I would have to train my right hand to hold down command + shift and hit the o.
- Word wrap is on by default
- Code suggestion was pretty bad
- Auto close brackets is off by default
- Opening a new window is again found under debug
- Can't handle projects that have more than 30,000

That last one was what broke the camel's back for me. While I understand that this was a decision to keep Brackets fast and nimble (which I admit it was). I thought it was kind of ridiculous. When I had two projects open, I received this message.

![](http://i.michaelsoolee.com/20150714-brackets-error.png)

Seeing that there was a reason that this message was shown, I clicked on the link to see what all the fuss was about. Towards the end of the document I saw this explanation.

> It's unlikely that the limit on project size will go away soon. Because Brackets is a lightweight code editor and not a large-scale IDE, it's not a high priority to support enormous projects with GBs of files.

Uhhhh...what?! Lightweight...Sublime Text weighs in at just 27MBs while Brackets is 111MBs on my machine. "code editor and not a large-scale IDE" so is Sublime Text and Atom but they can handle my 30,000+ files project and doesn't complain. Without much idea on what [Extract](http://blog.brackets.io/2014/11/04/brackets-1-0-and-extract-for-brackets-preview-now-available/) is or how it is integrated into Brackets (I downloaded the version without Extract), I think it is safe to say Brackets is a little more than just a "lightweight code editor".

Brackets definitely has speed going for it as well as some really good plugins. But it felt like an editor that was just afraid to be opinionated. What I mean by this, a lot of features you find in other editors like Atom or Sublime Text, turned on by default is turned off in Brackets &mdash; such as closing a bracket automatically or turning off word wrapping. So out of the box, I had to do a lot of tweaking to get it to my liking. I think it was also really confusing that so many menu items were grouped under the *debug* menu instead of other places like *file* for new windows or the preferences item has a "placeholder" but is actually found under *debug*. In putting so many things under the debug menu I just kept having the feeling that this was a beta, pre-1.0 piece of software.

Brackets had me at first with speed but lost me quickly with its confusing menu groupings and imposed limitations. I'm firing up Sublime Text to get some work done.