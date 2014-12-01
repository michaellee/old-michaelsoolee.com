---
layout: post
title: "Ember.js skip link component"
category: 'ember.js'
external: https://www.codehive.io/boards/pZUuwIk
---

One of the requirements for the project I'm currently working on is to make sure accessibility features are implemented so that users with disabilities may be able to navigate with keyboard or screen reader.

Here is a CodeHive Board that details how I created a custom component for skip links. One of the challenges of implementing a skip link in Ember.js is the fact that Ember uses the hash character in the URL to handle state changes. Skip links also adds a hash to the URL.

This makes for some adverse results, which is why I used a scrollto solution.
