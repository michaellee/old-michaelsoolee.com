---
layout: post
title: "Ember file structure should reflect route setup"
category: 'work'
link: https://www.codehive.io/boards/FdZ6BM8
date: 2015-07-16 11:58:00
---

I had a nested route setup in my Ember application but my file structure didn't reflect this. This resulted in not being able to reach the message route. Nesting the route and the template files to reflect the nested route in my router.js file fixed the problem.