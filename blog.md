---
layout: default
title: Blog
permalink: /blog/
---

<h1 class="page-title">Blog</h1>

<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <p class="post-meta">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time>
      {% if post.author %} · {{ post.author }}{% endif %}
    </p>
  </li>
  {% endfor %}
</ul>
