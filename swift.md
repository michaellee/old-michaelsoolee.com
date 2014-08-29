---
layout: page
title: Learning Swift
permalink: /learning/swift/
---

{% for post in site.swift  %}
  
  <a href="{{ post.url }}">{{ post.title }}</a>

{% endfor %}