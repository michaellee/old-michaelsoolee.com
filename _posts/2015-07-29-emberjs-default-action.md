---
layout: post
title: "Allowing default browser actions in Ember.js"
category: 'work'
link: https://www.codehive.io/boards/2cGrv-E
date: 2015-07-29 16:00:00
---

I had a couple of action helpers on some radio buttons hooked up. But when I had clicked on them, the actions would trigger but the radio buttons wouldn't go into the checked state. Meaning, you couldn't tell which was selected. Turns out this is something that Ember.js prevents by default when using an action helper. But the fix is simple.