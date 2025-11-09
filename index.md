---
layout: default
title: "Amy Lee's Tech Blog"
---

<style>
/* uppercase subtitles + more breathing room between categories */
.category-group {
  margin-bottom: 3rem; /* more space between groups */
}

.category-list {
  margin-left: 2.4em;
}

.post-date {
  opacity: 0.7;
  margin-right: 0.4rem;
}
</style>

{% assign categories = site.categories | sort %}
{% for cat in categories %}
  {% assign cat_name = cat[0] | upcase %}
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
