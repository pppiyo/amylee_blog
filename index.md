---
layout: default
title: "Amy Lee's Tech Blog"
---

<style>
/* Sleek hacker-style index page */
.category-group {
  margin-bottom: 2rem;
}

.category-title {
  color: #7fff00; /* neon hacker green */
  margin-bottom: 0.6rem;
  font-weight: bold;
  font-size: 1.1rem;
  text-transform: uppercase;
}

.category-list {
  list-style: none;
  padding-left: 1.2rem;
  margin: 0;
}

.category-list li {
  margin: 0.25rem 0;
}

.post-date {
  opacity: 0.6;
  margin-right: 0.5rem;
}
</style>

{% assign categories = site.categories | sort %}
{% for cat in categories %}
  {% assign cat_name = cat[0] %}
  {% assign posts = cat[1] | sort: "date" | reverse %}
  <div class="category-group">
    <div class="category-title">{{ cat_name }}</div>
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
