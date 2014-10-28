CSS allows you to animate elements based on property values. One of the properties that I animate often is the `height` of an element.

For example, height is what I animated to show and hide the menu in this Pen.

<p data-height="348" data-theme-id="0" data-slug-hash="tJCkb" data-default-tab="result" data-user="michaellee" class='codepen'>See the Pen <a href='http://codepen.io/michaellee/pen/tJCkb/'>tJCkb</a> by Michael Lee (<a href='http://codepen.io/michaellee'>@michaellee</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

But as you can see here using height isn't ideal, because the height would have to be an exact value. An exact value has to be given or you'll either get extra white space or some overflow issues.

Instead of height, you should animate `max-height` instead. When animating max-height, just make sure to give the final max-height a big enough value to make sure you don't have any content being cut off by the overflow rule.

<p data-height="296" data-theme-id="0" data-slug-hash="BIoac" data-default-tab="result" data-user="michaellee" class='codepen'>See the Pen <a href='http://codepen.io/michaellee/pen/BIoac/'>BIoac</a> by Michael Lee (<a href='http://codepen.io/michaellee'>@michaellee</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>

```sass
.PrimaryNav-container {
  ...
  max-height: 0;
  overflow: hidden;
  -webkit-transition: max-height 0.3s ease;
  -moz-transition: max-height 0.3s ease;
  transition: max-height 0.3s ease;
  ...
}

.PrimaryNav.PrimaryNav--isOpen .PrimaryNav-container {
  max-height: 300px;
}
```

On my browser, the rendered height of the container holding the link elments is 200px. But just to make sure I won't have any issues in other browsers, I gave max-height a value of 300px. This ensures me even if the height varies by a few pixels in a different browser, the animation will still look consistent across browsers.
