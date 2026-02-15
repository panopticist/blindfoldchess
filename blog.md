---
layout: default
title: Blog
---

<h1>Blog</h1>

<p>Updates on blindfold chess performances, players, history, and research.</p>

<ul class="post-list">
{% for post in site.posts %}
  <li>
    <h2 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <p class="post-meta">{{ post.date | date: "%B %d, %Y" }} • By {{ post.author }}</p>
    {% if post.excerpt %}
    <div class="post-excerpt">
      {{ post.excerpt }}
    </div>
    {% endif %}
  </li>
{% endfor %}
</ul>
