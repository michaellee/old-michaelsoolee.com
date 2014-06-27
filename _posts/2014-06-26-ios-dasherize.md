---
layout: post
title: "A Simple Dasherize Method in Objective-C"
categories: programming
response: "If this method is helpful to you or if you can improve upon it, let me know."
---

I've recently been diving into iOS programming and decided to make a simple directory app of people I work with. The app parses a locally stored JSON file that has the name and role of a person. I'm also hosting some profile photos of the people in a Dropbox folder.

Instead of adding another key/value pair to my JSON file for every person, I wanted to just use their name to grab their corresponding profile photo from Dropbox.

Each photo is stored on Dropbox with a filename syntax of _firstname-lastname.jpg_. The syntax of each name in the JSON file is _FirstName LastName_.

I don't think Objective-C has computed values like Ember.js does. So I created a simple dasherize method that returns a string in the format that I need for the Dropbox photos.

<script src="https://gist.github.com/michaellee/7a42df8d35b44b139ca3.js"></script>

First, the method creates a lowercase copy of the string you pass to the method. Then each occurrence of a space is replaced with a `-`. Finally a dasherized string is returned, which I can stick in a formatted string to pull the photo from Dropbox.

The method isn't as robust as Ember.js' <a href="http://emberjs.com/api/classes/Ember.String.html#method_dasherize" target="_blank">dasherize method</a>, so I can definitely improve upon it to handle the same inputs Ember.js' method does.
