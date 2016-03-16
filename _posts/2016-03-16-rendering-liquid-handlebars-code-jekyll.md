---
layout: post
title: "Rendering Liquid and Handlebars Expressions in Jekyll Code Blocks"
category: work
---

Sharing blocks of code is something that I do regularly on my site as well as other sites that I blog on.

Liquid (templating library for Jekyll) and Handlebars expressions (templating library found in Ember applications) use the curly braces to render content. When placing them in code blocks in Jekyll, Jekyll will by default try to render them as expressions instead of just raw code.

To fix this issue and render the code block with with Liquid and Handlebars expressions as code and not for Jekyll to try to render as content, you can use the `{% raw %}{% raw %}{% endraw %}` expression.
