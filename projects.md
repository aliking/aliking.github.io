---
layout: page
title: Projects
description: Things I've built — useful, weird, or both.
permalink: /projects/
---

A collection of software projects, side experiments, and things that felt important to build at the time.

{% assign all_projects = site.projects %}
{% if all_projects.size > 0 %}
<div class="grid-2" style="margin-top: 2rem;">
  {% assign colors = "teal,purple,pink,yellow" | split: "," %}
  {% for project in all_projects %}
  <a href="{{ project.url | relative_url }}" style="text-decoration: none; display: block;">
    <div class="card">
      <h3 class="card-title">{{ project.title }}</h3>
      {% if project.status %}
      <p class="card-meta">{{ project.status }}</p>
      {% endif %}
      <p class="card-desc">{{ project.description }}</p>
      {% if project.tech %}
      <div class="card-tags">
        {% for t in project.tech limit: 5 %}
        {% assign ci = forloop.index0 | modulo: 4 %}
        <span class="tag tag-{{ colors[ci] }}">{{ t }}</span>
        {% endfor %}
      </div>
      {% endif %}
    </div>
  </a>
  {% endfor %}
</div>
{% else %}
<p style="color: #9898b8; font-style: italic; margin-top: 2rem;">Projects incoming — check back soon.</p>
{% endif %}
