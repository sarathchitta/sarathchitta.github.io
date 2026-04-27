---
layout: default
title: Blog
permalink: /blog/
---

## Blog Archive

{% if site.posts.size > 0 %}
<ul class="latest-posts">
  {% for post in site.posts %}
  <li class="latest-post-item">
    <div class="latest-post-header">
      <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a>
      <span class="latest-post-meta">{{ post.date | date: "%B %-d, %Y" }}</span>
    </div>
    <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 220 }}</p>
    {% if post.tags and post.tags.size > 0 %}
    <p class="post-tags">
      {% for tag in post.tags %}
      <span class="post-tag">{{ tag }}</span>
      {% endfor %}
    </p>
    {% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p class="latest-posts-empty">No posts published yet. Check back soon.</p>
{% endif %}
