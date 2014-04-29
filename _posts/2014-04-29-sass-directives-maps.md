---
layout: post
title:  "Sass Directives and Maps"
categories: css
---

I've started playing around with Sass Directives and Maps; which the latter was recently introduced in <a href="http://sass-lang.com/documentation/file.SASS_CHANGELOG.html#330_7_march_2014" target="_blank">Sass 3.3</a>. If you're familiar with languages like Javascript or Ruby, a Sass Map is the equivalent of a Hash; they store key/value pairs.

One of the first things I did when I discovered Sass Directives and Maps were to convert my color variables into a map and use a loop to quickly generate utility style blocks in the manner of OOCSS.

Here's an example of going from using variables to using a Map and a loop.

Before:

    $black: #000;
    $white: #fff;
    $red: #eb6f60;
    $blue: #45aee7;
    $purple: #837abd;

    .bg--black{ background-color: $black; }
    .bg--white{ background-color: $white; }
    .bg--red{ background-color: $red; }
    .bg--blue{ background-color: $blue; }
    .bg--purple{ background-color: $purple; }

After:

    $colors:(
      black: #000,
      white: #fff,
      red: #eb6f60,
      blue: #45aee7,
      purple: #837abd,
    );
    
    @each $color, $value in $colors{
      .bg--#{$color}{ background-color: #{$value}; }
    }

Both would create this final CSS:

    .bg--black{ background-color: #000; }
    .bg--white{ background-color: #fff; }
    .bg--red{ background-color: #eb6f60; }
    .bg--blue{ background-color: #45aee7; }
    .bg--purple{ background-color: #837abd; }

Awesome right? Less code and you won't miss any colors you define in the map. But what if you want to use a color value from the map?

It'd look something like this:

    .button--blue{
      border: 1px solid map-get($colors, blue);
    }

The `map-get` function with two parameters seem a bit verbose when prior to maps I just called `$variableName`.

At first, I thought I could just use another loop to create variables on the fly.

    @each $color, $value in $colors{
      $#{$color}: $value;
    }

But it turns out that this is invalid and won't compile at all. <a href="https://twitter.com/johnwlong" target="_blank">John Long</a> from The Sass Way confirmed <a href="https://twitter.com/hellomichaellee/status/461160399526977537" target="_blank">this as well</a>.

After some conversations with my buddy, <a href="https://twitter.com/joelpdesigns" target="_blank">Joel</a>. He suggested I write out the variables again, then create it's duplicate key but use the variable value to create the map.

    $black: #000;
    $white: #fff;
    $red: #eb6f60;
    $blue: #45aee7;
    $purple: #837abd;
    
    $colors:(
      black: $black,
      white: $white,
      red: $red,
      blue: $blue,
      purple: $purple,
    );

This way, I can update any values for a variable I created and the map would update and generate my utilities accordingly. I can still use `$variableName` instead of `map-get($map, value)` for use in style blocks.

This feels a bit cumbersome to maintain but with this solution I can still use variable names and I get the benefits of Maps and Sass Directives for creating OOCSS utilities.
