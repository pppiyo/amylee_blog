---
layout: default
title: "Amy Lee's Tech Blog"
---

<style>
/* Reduce the big header spacing below the GitHub button */
header {
  margin-bottom: 1.2rem !important;
}

/* Align category titles with the built-in >> markers */
.category-list {
  margin-left: 0; /* reset */
  padding-left: 2.4em; /* tweak this until "./" aligns visually with >> */
}

.post-date {
  opacity: 0.7;
  margin-right: 0.4rem;
}

/* Optional: if you later decide to remove >>, uncomment below
li::before { content: none !important; }
*/
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
