---
layout: default
title: Home
---

<section class="hero">
  <p class="hero-eyebrow">// hello, world</p>
  <h1 class="hero-title">aliking</h1>
  <p class="hero-sub">
    Software developer, tinkerer, and maker of things that probably shouldn't exist —
    but are more interesting because they do.
  </p>
  <div class="hero-cta">
    <a href="{{ '/projects' | relative_url }}" class="btn btn-primary">View Projects</a>
    <a href="{{ '/about' | relative_url }}" class="btn btn-outline">About Me</a>
  </div>
</section>

<div class="terminal">
  <div class="terminal-bar">
    <span></span><span></span><span></span>
  </div>
  <div class="terminal-line">
    <span class="prompt">❯ </span><span class="cmd">whoami</span>
  </div>
  <div class="terminal-line">
    <span class="out acc">aliking</span>
  </div>
  <div class="terminal-line">&nbsp;</div>
  <div class="terminal-line">
    <span class="prompt">❯ </span><span class="cmd">cat interests.txt</span>
  </div>
  <div class="terminal-line">
    <span class="out">software engineering · weird side projects · open source</span>
  </div>
  <div class="terminal-line">
    <span class="out">hardware hacking · generative art · overthinking things</span>
  </div>
  <div class="terminal-line">&nbsp;</div>
  <div class="terminal-line">
    <span class="prompt">❯ <span class="acc">_</span></span>
  </div>
</div>

{% assign recent_posts = site.posts | limit: 3 %}
{% if recent_posts.size > 0 %}
<section>
  <p class="section-label">// recent posts</p>
  <h2 class="section-title">Writing</h2>
  <ul class="post-list">
    {% for post in recent_posts %}
    <li class="post-item">
      <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
      <div>
        <a class="post-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
        {% if post.excerpt %}
        <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
        {% endif %}
      </div>
    </li>
    {% endfor %}
  </ul>
  <a href="{{ '/blog' | relative_url }}" class="btn btn-outline" style="margin-top: 1rem;">All posts →</a>
</section>
{% endif %}

{% assign featured = site.projects | where: "featured", true | limit: 3 %}
{% if featured.size > 0 %}
<div class="ornament">✦ · · ✦ · · ✦</div>
<section>
  <p class="section-label">// selected work</p>
  <h2 class="section-title">Projects</h2>
  <div class="grid-2">
    {% for project in featured %}
    <a href="{{ project.url | relative_url }}" style="text-decoration: none; display: block;">
      <div class="card">
        <h3 class="card-title">{{ project.title }}</h3>
        <p class="card-desc">{{ project.description }}</p>
        {% if project.tech %}
        <div class="card-tags">
          {% assign colors = "teal,purple,pink,yellow" | split: "," %}
          {% for t in project.tech limit: 4 %}
          {% assign ci = forloop.index0 | modulo: 4 %}
          <span class="tag tag-{{ colors[ci] }}">{{ t }}</span>
          {% endfor %}
        </div>
        {% endif %}
      </div>
    </a>
    {% endfor %}
  </div>
  <a href="{{ '/projects' | relative_url }}" class="btn btn-outline" style="margin-top: 2rem;">All projects →</a>
</section>
{% endif %}
