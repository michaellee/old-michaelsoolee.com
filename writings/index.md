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
    ## {{this_year}}
    ### {{ this_month }}
    <ul>
    {% endif %}

    <li><a href="{{ post.url }}">{{ post.title }}</a></li>

    {% if forloop.last %}
    </ul>
    {% else %}
      {% if this_year != next_year %}
      </ul>
      ## {{this_year}}
      ### {{ this_month }}
      <ul>
      {% else %}    
        {% if this_month != next_month %}
        </ul>
        ### {{ this_month }}
        <ul>
      {% endif %}
    {% endif %}
  {% endif %}
{% endfor %}
