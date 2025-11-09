---
layout: default
title: Amy Lee's Tech Blog
---

<style>
/* small tweaks just for this page */
.category-group {
  margin-bottom: 2rem;
}

.category-title {
  margin-bottom: 0.25rem;
}

.category-list {
  list-style: none;
  padding-left: 0;
  margin-top: 0.5rem;
}

.category-list li {
  margin: 0.15rem 0;
}

.category-list li::before {
  content: ">> ";
  margin-right: 0.35rem;
}

.post-date {
  opacity: 0.7;
  margin-right: 0.35rem;
}
</style>

# Notes by topic

{% assign categories = site.categories | sort %}
{% for cat in categories %}
  {% assign cat_name = cat[0] %}
  {% assign posts = cat[1] | sort: "date" | reverse %}
  <div class="category-group">
    <h2 class="category-title">{{ cat_name }}</h2>
    <ul class="category-list">
      {% for post in posts %}
        <li>
          <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span>
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </li>
      {% endfor %}
    </ul>
  </div>
{% endfor %}
