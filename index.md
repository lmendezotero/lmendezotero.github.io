---
layout: default
author_profile: true
title: Inicio
---

<h2>Entradas</h2>
<ul style="list-style-type: none; padding-left: 0;">
  {% for post in site.posts %}
    <li style="margin-bottom: 1.5em;">
      <strong><a href="{{ post.url | relative_url }}">{{ post.title }}</a></strong><br>
      {{ post.date | date: "%d %b %Y" }}{% if post.subtitle %} - {{ post.subtitle }}{% endif %}
      <div style="margin-top: 0.4em;">
        {% if post.categories %}
          <div>
            {% for category in post.categories %}
              <span style="
                display: inline-block;
                background-color: #1D5F5B;
                color: white;
                padding: 3px 8px;
                border-radius: 12px;
                font-size: 0.8em;
                font-weight: 600;
                margin-right: 5px;
                user-select: none;
              ">
                {{ category }}
              </span>
            {% endfor %}
          </div>
        {% endif %}
      </div>
    </li>
  {% endfor %}
</ul>
