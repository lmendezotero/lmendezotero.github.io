---
layout: default
author_profile: true
title: Inicio
---

<h2>Entradas</h2>
<ul class="post-list">
  {% for post in site.posts %}
    <li class="post-item">
      <h3 class="post-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="post-meta">
        {{ post.date | date: "%d %b %Y" }}{% if post.subtitle %} – {{ post.subtitle }}{% endif %}
      </p>
      <div class="post-categories">
        {% if post.categories %}
          {% for category in post.categories %}
            <span class="category-badge">{{ category }}</span>
          {% endfor %}
        {% endif %}
      </div>
    </li>
  {% endfor %}
</ul>
