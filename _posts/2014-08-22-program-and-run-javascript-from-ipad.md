---
layout: post
title: "Program and Run Javascript from your iPad"
category: programming
---

Lately, I've been experimenting with programming from my iPad. Thanks to Panic's app, [Prompt](https://itunes.apple.com/us/app/prompt/id421507115?mt=8&uo=4&at=11l9EG) I can be sitting in bed and SSHed to my laptop that's sitting in the living room. Once I've SSHed into my laptop, I fire up my [current editor of choice, Vim]({{site.url}}/learning-vim/) and start coding away.

The other night I was wondering if there was some way to use my iPad setup to write Javascript. I assumed since I've seen Javascript mostly running in my browser, I wouldn't be able to write and test Javascript from the command line.

After doing some searching, I came across that Node.js allows you to run Javascript from the command line. This was great, because I could write Javascript from my iPad and then run the files from the command line without ever needing a browser.

## The Setup

On your iPad you want to install an app that'll let you SSH to another machine. As mentioned earlier I use the app, [Prompt by Panic](https://itunes.apple.com/us/app/prompt/id421507115?mt=8&uo=4&at=11l9EG).

On the machine that I SSH to from my iPad, I have Vim setup to my likings. Vim allows me to write code from the iPad in a text-editor that I'm familiar with in my desktop.

If you already have Node.js installed on your machine. You should already have the ability to run Javascript from Terminal. Simply navigate to the .js file you want to run, and use node's CLI tool to run the file.

The syntax is `node filename.js`.

If you don't have Node.js installed, simply [download node](http://nodejs.org/download/) and by installing the Node.js package it should automatically make the node CLI available in your terminal.
