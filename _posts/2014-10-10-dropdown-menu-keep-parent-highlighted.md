---
layout: post
title: "Highlighted Parent Item in Dropdown Menus"
categories: css programming
---

Dropdown menus are a UI design pattern you see on websites. Most commonly, they are used in a site's nav.

While implementing a dropdown menu in a project I thought to myself, it'd be great if the parent item of the submenu was highlighted. This is so that even though the parent item isn't being hovered over, there would be a visual cue that the current submenu I'm navigating belongs to it's parent.

Here's an example of what I'm trying to accomplish:

![](https://dl.dropboxusercontent.com/u/1228961/michaellee/2014/10%20-%20October/dropdown.png)

Here's an example of the HTML I used to setup my menu.

```html
<nav role='navigation'>
  <ul class="menu">
    <li class="menu-item">
      <a href="javascript:;">About</a>
    </li>
    <li class="menu-item">
      <a href="javascript:;">Works<span class="ion-arrow-down-b menu-item-icon"></span></a>
      <ul class="menu-submenu">
        <li class="menu-submenu-item"><a href="javascript:;">Design</a></li>
        <li class="menu-submenu-item"><a href="javascript:;">Dev</a></li>
        <li class="menu-submenu-item"><a href="javascript:;">Writings</a></li>
      </ul>
    </li>
    <li class="menu-item">
      <a href="javascript:;">Contact Us</a>
    </li>
  </ul>
</nav>
```

As you can see, it's a simple unordered-list menu. In the second list-item, you see that I have another unordered-list that is used for the submenu.

```html
...
<li class="menu-item">
  <a href="javascript:;">Works<span class="ion-arrow-down-b menu-item-icon"></span></a>
  <ul class="menu-submenu">
    <li class="menu-submenu-item"><a href="javascript:;">Design</a></li>
    <li class="menu-submenu-item"><a href="javascript:;">Dev</a></li>
    <li class="menu-submenu-item"><a href="javascript:;">Writings</a></li>
  </ul>
</li>
...
```

When selecting an item from the submenu, I want the parent item to also be highlighted. This could be accomplished with CSS.

Here's the chunk of my code that accomplishes this.

```css
...
.menu-item{
  display: inline-block;
  margin-left:   0.5em;
  margin-right:  0.5em;
  
  position: relative;
  padding-bottom: 10px;
  a{
    color: #333;
  }
  &:hover .menu-submenu{
    display: block;
  }
  &:hover > a{
    color: #4F8EF7;
  }
}
...
```

Specifically, the rule when `.menu-item` is hovered over. The `:hover` rule is saying, when `.menu-item` is being hover, then change the color of the immediate child `a` elements.

In placing the `:hover` rule on the element that encompasses the menu item link and the submenu &mdash; instead of the actual link &mdash; you're able to achieve having the parent item stay highlighted while you hover over the submenu.

Here's a demo of the dropdown menu with highlighting parent items.

<p data-height="268" data-theme-id="0" data-slug-hash="mzJFi" data-default-tab="result" data-user="michaellee" class='codepen'>See the Pen <a href='http://codepen.io/michaellee/pen/mzJFi/'>Highlighted Parent Item in Dropdown Menus</a> by Michael Lee (<a href='http://codepen.io/michaellee'>@michaellee</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>
