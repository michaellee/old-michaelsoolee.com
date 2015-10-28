---
layout: post
title: "Almost forgot"
category: "work"
date: 2015-10-27 23:00:00
---

Earlier today I asked a [question on CodeHive regarding Ember.js' `link-to`
helper](https://www.codehive.io/boards/DfnxGw8). I had a route set up that was hyphenated. Using the helper, I had passed in the route that was hyphenated and it was erroring out. I tried a few variations, assuming that maybe I was passing in the wrong syntax to the helper. I tried reading over the docs for the helper and even did a quick Google search.

I couldn't find anything. So, naturally I figured this would be a good chance to ask a question on CodeHive. I created the Board, published it and then tweeted it out, hoping that some Ember guru would reply back. In the mean time I went back to the code and tried to back track a little. I deleted the route, instead of using a hyphenated name, I used camelcase. As expected, it worked.

Confused, I decided to try the hyphenated version once more. This time it worked. I undid my changes to see what I did differently the first time. Looking at my router file, it turns out I had defined the path to expect a dynamic segment but didn't reflect that in my `link-to` helper when trying to link to that route.

I felt embarrased actually at such a noob mistake. Feeling self-conscious, I
contemplated deleting my question on CodeHive and deleting the tweet to the
question to save myself from embarrassment. But it was at this time that I remembered this is the exact reason why I started CodeHive.

Programming is tough. I made a mistake, but I learned from this mistake. And that's an important trait for a programmer, the ability to self-correct.

I think as programmers, we should encourage new or beginner programmers to mull over their problems and guide them to problem-solve and learn to self-correct, instead of criticizing them on how noob of a job they've done.

Programming ain't easy. I've been programming for over 10 years and it still ain't easy. And that's also what makes it fun and rewarding.

Instead of deleting my question, I actually left it up on CodeHive and left
myself feedback on the Board. Sharing exactly what I was running into and how I
was able to solve the problem. It serves as a reminder to me that CodeHive is a
place where asking noob questions is encouraged no matter how long you've been
in the programming game and occassionally if you solve
the problem to your own question, dope and you should totally share how you overcame it.
