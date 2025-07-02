---
layout: default
author_profile: true
title: Inicio
---

<h2>Entradas</h2>
<ul class="post-list">
  {% for post in site.posts %}
    <li class="post-item">
      <div class="post-title">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </div>
      <div class="post-meta">
        {{ post.date | date: "%d %b %Y" }}{% if post.subtitle %} - {{ post.subtitle }}{% endif %}
      </div>
      {% if post.categories %}
        <div class="post-categories">
          {% for category in post.categories %}
            <span class="category-badge">{{ category }}</span>
          {% endfor %}
        </div>
      {% endif %}
    </li>
  {% endfor %}
</ul>
