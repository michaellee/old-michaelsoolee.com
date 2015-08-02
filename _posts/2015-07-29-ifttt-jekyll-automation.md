---
layout: post
title: "How I automate some of my social networking with IFTTT"
category: 'work'
date: 2015-07-29 20:00:00
---

On this site, I use a static-site generator called [Jekyll](http://jekyllrb.com/) to maintain and publish posts. It is definitely not the easiest setup in publishing a blog. But it is the system that has kept me the most consistent in writing and because of how it is setup, it appeals to my nerdiness.

The site is statically generated, meaning there is no database. Jekyll generates each post as a html file and you upload that to your web server. Because of this, there is no need for a complex server to host my site. I'm actually hosting my site using GitHub Pages. A pro and con of this setup is there are no plugins to do things like automatically publish your new posts to your social networks.

Thankfully there is a sweet service called [IFTTT](https://ifttt.com/) (which stands for *If This Then That*). IFTTT is a great service to automate actions between two different apps using recipes that follow the simple statement of, if this then that. I've created a couple of recipes that helps automate some of my social networking.

<!--more-->

Prior to discovering IFTTT, after I published a post, I would grab the URL and the title and open Twitter and LinkedIn and publish my new post there. Although it'd take me but five minutes or less to do this, I wanted to remove that step altogether from my posting workflow.

To accomplish this, I use recipes that are made up of watching my site's RSS feed for new items, since Jekyll automatically creates a RSS file. When a new item is found, then IFTTT creates a new update using the title and URL and post it up to their respective social media accounts.

## Here's step-by-step how I've created the Twitter IFTTT recipe

First, [click on create a new recipe](https://ifttt.com/myrecipes/personal/new) and you should be presented with the IFTTT recipe statement.

![](http://i.michaellee.co/20150729-ifttt-01.png)

Click on the *this* statement, and then you'll be presented with a bunch of channels (what IFTTT calls applications) to select from. Filter this list, by typing in **RSS** in the search field.

![](http://i.michaellee.co/20150729-ifttt-02.png)

Once RSS shows up, click on the *RSS channel*.

![](http://i.michaellee.co/20150729-ifttt-03.png)

Now select the trigger *New Feed Item*. What this does is, it'll check your RSS feed and check to see if there are any new items added. If so then trigger your recipe.

![](http://i.michaellee.co/20150729-ifttt-04.png)

You'll be asked to provide the URL of your RSS feed. Fill this in and then create the trigger. Once the trigger is created, you'll be brought back to your statement to create the *that* portion of the recipe.

![](http://i.michaellee.co/20150729-ifttt-05.png)

Clicking on *that* will bring you to a new listing of channels to create your action.

![](http://i.michaellee.co/20150729-ifttt-06.png)

This time, you'll want to search for *Twitter*. Once Twitter comes up, select the channel.

![](http://i.michaellee.co/20150729-ifttt-07.png)

When you're presented with the actions, select the one that says *Post a tweet*

![](http://i.michaellee.co/20150729-ifttt-08.png)

After selecting your action, you'll be given the option to fine tune your tweet's text. In my tweet, I just have the post title and post link separated by a space.

![](http://i.michaellee.co/20150729-ifttt-09.png)

Once you've created your action, you'll be brought to a screen to review your recipe. If you're satisfied with what you've got, select *Create Recipe*.

![](http://i.michaellee.co/20150729-ifttt-10.png)

Now look at that, a nice shiny new IFTTT recipe that'll watch my Jekyll generated site's RSS and auto tweet my latest post's title and URL.

There are two tidbits, I'd like to also share. First, after publishing a post, the recipe doesn't trigger instantaneously. I believe IFTTT has their servers set up to trigger recipes on a set interval. I've got IFTTT on my phone to notify me when a recipe runs and <del>I believe the recipes usually trigger within five minutes of posting</del> <ins>according to IFTTT most recipes will poll for [new trigger data every 15 mins](https://ifttt.com/wtf)</ins>.

The second tidbit is, by default, IFTTT will shorten links and uses their shortened URL when posting things with a link. I'm not a big fan of shortened URLs, especially if they are unbranded. Thankfully there is an option that you can actually have IFTTT not shorten links.

To do this, you'll want to go to *Preferences* found under your account. Then if you scroll down, you'll find an option for *URL Shortening*.

![](http://i.michaellee.co/20150729-ifttt-11.png)

**Unchecking** the option *Auto shorten URLs* will leave your links untouched and in their original form. Sweet.

If you're like me and use a static-site generator like Jekyll, IFTTT can be used in a powerful way to automate some of your social networking and save you time in your publishing workflow.
