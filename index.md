---
layout: default
title: "Amy Lee's Tech Blog"
---

<style>
/* indent lists so ">>" starts under the text after "./ " */
.category-list {
  margin-left: 2.4em; /* tweak this value if you want finer alignment */
}

.post-date {
  opacity: 0.7;
  margin-right: 0.5rem;
}
</style>

{% assign categories = site.categories | sort %}
{% for cat in categories %}
  {% assign cat_name = cat[0] %}
  {% assign posts = cat[1] | sort: "date" | reverse %}

## ./ {{ cat_name }}

<ul class="category-list">
  {% for post in posts %}
  <li>
    <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
  {% endfor %}
</ul>

{% endfor %}
