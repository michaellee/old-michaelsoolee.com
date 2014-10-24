#CSS nth-child Numbers and Expressions

Rows of elements in columns are a common UI pattern you see throughout websites.

Your HTML markup might look something like this.

```html
<div class="items">
  ...
  <div class="item">
    <div class="item-box"></div>
  </div>
  <div class="item">
    <div class="item-box"></div>
  </div>
  <div class="item">
    <div class="item-box"></div>
  </div>
  <div class="item">
    <div class="item-box"></div>
  </div>
  <div class="item">
    <div class="item-box"></div>
  </div>
  ...
</div>
```

Add in some CSS styling.

```css
*, *::before, *::after{
  box-sizing: border-box;
}

.item{
  width: 25%;
  height: 100px;
  float: left;
  display: block;
  padding-right: 20px;
  margin-top: 20px;
}

.item-box{
  background: #CCC;
  width: 100%;
  height: 100px;
}
```

Presto! We've got some gray boxes in a row, separated into columns.

<p data-height="403" data-theme-id="0" data-slug-hash="lCpwq" data-default-tab="result" data-user="michaellee" class='codepen'>See the Pen <a href='http://codepen.io/michaellee/pen/lCpwq/'>lCpwq</a> by Michael Lee (<a href='http://codepen.io/michaellee'>@michaellee</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

But, we're not crazy about the first row of elements also having a top-margin. If we had any other element above the `.items` container, and that element had some bottom margin. Then we'd have some odd spacing.

To get rid of the top-margin, we're going to remove the top-margin of the first 4 elements in the top row. To do this, we'll use the CSS pseudo-selector &mdash; `:nth-child()`.

The `:nth-child()` pseudo-selector allows you to pass in either a _number_ or an _expression_ in the parenthesis.

So for example if we had `.item:nth-child(1)`, this would apply styling to the very first `.item` element. You can also pass in something like `.item:nth-child(4n)` and the styles would apply to every fourth `.item` element.

The way this works is, some simple algebra. `n` is substituted with zero and then all the preceeding positive numbers. 

So in the example of 4n, it translates to:

```
4 * 0 = 0
4 * 1 = 4
4 * 2 = 8
and so on...
```

In order to get rid of the top-margin we'll pass in this expression `-n + 4`. What this expression will do is start from the fourth `.item` element and go down to the first `.item` element and apply the styles we want. The math works like this:

```
-0 + 4 = 4
-1 + 4 = 3
-2 + 4 = 2
-3 + 4 = 1
```

I'll apply the pseudo-selector to my code and some style rules and the result is no top-margin in the first row.

```css
.item:nth-child(-n + 4){
  margin-top: 0;
}
```

<p data-height="376" data-theme-id="0" data-slug-hash="aBsHv" data-default-tab="result" data-user="michaellee" class='codepen'>See the Pen <a href='http://codepen.io/michaellee/pen/aBsHv/'>aBsHv</a> by Michael Lee (<a href='http://codepen.io/michaellee'>@michaellee</a>) on <a href='http://codepen.io'>CodePen</a>.</p>

We're getting there, but now I'm not too crazy about the last element in each row, having spacing. I don't mind spacing between each element but I want elements on both ends of each row to be flush with the parent container &mdash; which in this case is the entire browser window.

To do this, we'll use this expression `4n`. What this expression will do is grab every fourth element &mdash; the last element in each row &mdash; and apply the styles I define. The math works like this:

```
4 * 0 = 0 (Which doesn't exist)
4 * 1 = 4
4 * 2 = 8
etc.
```

So I'll add this it to my code with some styling.

```css
.item:nth-child(4n){
  padding-right: 0;
}
```

And now I've got rows of elements in columns with no spacing at the top and no spacing on either sides of each row. We've only got space inbetween each element in a row.

<p data-height="376" data-theme-id="0" data-slug-hash="ymbcB" data-default-tab="result" data-user="michaellee" class='codepen'>See the Pen <a href='http://codepen.io/michaellee/pen/ymbcB/'>ymbcB</a> by Michael Lee (<a href='http://codepen.io/michaellee'>@michaellee</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>

That's more like it!

_This tip is part of the 100CodeTips series. To check out all the other tips in the series, search `100CodeTips` in the search bar or follow the hashtag `#100CodeTips` on Twitter_
