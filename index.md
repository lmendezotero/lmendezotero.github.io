---
layout: default
author_profile: true
title: Inicio
---

<h2>Entradas</h2>
<ul>
  {% for post in site.posts %}
    <li style="margin-bottom: 1.5em;">
      <strong><a href="{{ post.url | relative_url }}">{{ post.title }}</a></strong><br>
      {{ post.date | date: "%d %b %Y" }}{% if post.subtitle %} - {{ post.subtitle }}{% endif %}
      <div style="margin-top: 0.4em;">
        {% if post.categories %}
          <span style="font-weight: 600; color: #333;">
            {{ post.categories | join: "    |    " }}
          </span>
        {% endif %}
      </div>
    </li>
  {% endfor %}
</ul>
