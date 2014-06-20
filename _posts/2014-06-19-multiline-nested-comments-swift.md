---
layout: post
title:  "Multiline Nested Comments in Swift"
categories: swift
---

While looking through [The Swift Programming Language](https://itunes.apple.com/us/book/swift-programming-language/id881256329?mt=11&uo=4&at=11l9EG) iBook, I came across `comments` in Swift.

Swift supports nested multiline comments. Upon reading and looking at the code sample, I wondered to myself what this could be useful for. Then right after the code sample, this paragraph gave a great use case, one that I ran into before in the past.

> Nested multiline comments enable you to comment out large blocks of code quickly and easily, even if the code already contains multiline comments.

There's been many times where I've got a block of code with a few scattered, single lines commented out. Then I'd decide I wanted to comment out the whole block of code and I'd have to go through and first uncomment the single lines and then comment out the block. But what if after commenting out the block, I went and wrote some new code somewhere else and I wanted to uncomment that block again and leave out the previously single-lined commented code?

Undoing to the point before I commented out the block of code would mean I'd lose any changes I made after commenting previously and trying to recall mentally where those single-lined comments were...well yeah my memory doesn't serve me that well. Swift's solution for nested comments is very helpful to overcome scenarios like this.

I'm not sure if Swift's style of multiline nested comments are available in other programming languages but I'm beginning to delight in Swift.