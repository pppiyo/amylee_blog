---
layout: default
title: Amy Lee's Tech Blog
---
# ./ Notes
<ul>
  {% for category in site.categories %}
    <h2>{{ category[0] | capitalize }}</h2>
    <ul>
      {% for post in category[1] %}
        <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
      {% endfor %}
    </ul>
  {% endfor %}
</ul>
