---
layout: page
title: Blog
description: Notes, walkthroughs, and occasional opinions.
permalink: /blog/
---

{% if site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts %}
  <li class="post-item">
    <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
    <div>
      <a class="post-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      {% if post.excerpt %}
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
      {% endif %}
      {% if post.tags and post.tags.size > 0 %}
      <div style="margin-top: 0.5rem; display:flex; gap: 0.25rem; flex-wrap: wrap;">
        {% for tag in post.tags %}
        <span class="tag tag-purple">{{ tag }}</span>
        {% endfor %}
      </div>
      {% endif %}
    </div>
  </li>
  {% endfor %}
</ul>
{% else %}
<p style="color: #9898b8; font-style: italic; margin-top: 2rem;">Nothing published yet — watch this space.</p>
{% endif %}
