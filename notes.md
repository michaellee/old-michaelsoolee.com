---
layout: page
title: Notes
permalink: /notes
---

These are a set of notes I've created while learning something new. I've created these to reference when I need them.

{% for note in site.notes %}
<a href="{{ note.url | prepend: site.baseurl }}">{{ note.title }}</a>
{% endfor %}
