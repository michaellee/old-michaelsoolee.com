---
layout: post
title: "Custom Shapes in iOS"
categories: programming
---

The other day, my partner challenged me that I should draw the custom shape elements I was using for Project Z with code instead of relying on transparent PNGs that I created in Photoshop.

After some thought, I accepted the challenge and sought out how to draw custom shapes in iOS. After doing a quick search, I discovered iOS has a vector drawing class called `UIBezierPath`. The bezier path would be used to define the path of the new shape, and then the shape would be rendered using the `CAShapeLayer` class.

I was surprised to find that drawing shapes with UIBezierPath is a lot like drawing SVG shapes by hand for the web. You have commands like move to a point and then draw from one point to another point. Lately I've been programmatically drawing web SVGs, so creating my custom shape in iOS was pretty straightforward.

The result was great, the shape was uber crisp and I can control the fill color with floating point precision.

If you're trying to use shapes in your iOS app, have a look at <a href="https://developer.apple.com/library/ios/documentation/2ddrawing/conceptual/drawingprintingios/BezierPaths/BezierPaths.html" target="_blank">`UIBezierPaths`</a>. 
