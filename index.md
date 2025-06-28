---
layout: default
author_profile: true
title: Inicio
---

<h2>Entradas</h2>
<ul>
  {% for post in site.posts %}
    <li style="margin-bottom: 1em;">
      <strong><a href="{{ post.url | relative_url }}">{{ post.title }}</a></strong><br>
      {{ post.date | date: "%d %b %Y" }}{% if post.subtitle %} - {{ post.subtitle }}{% endif %}
    </li>
  {% endfor %}
</ul>
