---
layout: default
title: Other writings / Michael Lee
---

# Other writings

{% for post in site.posts  %}
  
  {% capture this_year %}{{ post.date | date: "%Y" }}{% endcapture %}
  {% capture this_month %}{{ post.date | date: "%B" }}{% endcapture %}
  {% capture next_year %}{{ post.previous.date | date: "%Y" }}{% endcapture %}
  {% capture next_month %}{{ post.previous.date | date: "%B" }}{% endcapture %}

  {% if forloop.first %}
  <h2>{{this_year}}</h2>
  <h3>{{ this_month }}</h3>
  {% endif %}

  <a href="{{ post.url }}">{{ post.title }}</a>

  {% if forloop.last %}
    {% else %}
      {% if this_year != next_year %}
  <h2>{{next_year}}</h2>
  <h3>{{ next_month }}</h3>
    {% else %}    
      {% if this_month != next_month %}
  <h3>{{ next_month }}</h3>
      {% endif %}
    {% endif %}
  {% endif %}
{% endfor %}
