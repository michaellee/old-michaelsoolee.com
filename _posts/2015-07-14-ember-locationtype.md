---
layout: post
title: "Changing an ember-cli app's locationType"
category: 'work'
link: https://www.codehive.io/boards/2rsmkYc
date: 2015-07-14 16:35:00
---

This was driving me nuts. Since by default the ember-cli will set locationType to `auto`. Which I assume will leave it up to the app to determine whether the browser has support for [session history](http://caniuse.com/#feat=history). Only problem is this wasn't working for me. I do know ember's [hashLocation](http://emberjs.com/api/classes/Ember.Location.html#toc_hashlocation) did work for me in the past, so I changed locationType to `hash`.