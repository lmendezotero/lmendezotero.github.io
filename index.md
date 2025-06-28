---
layout: default
author_profile: true
title: Inicio
---

<h2>Entradas</h2>
<ul>
  {% for post in site.posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%d %b %Y" }}</li>
  {% endfor %}
</ul>

