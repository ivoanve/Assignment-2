---
layout: default
title: Home
---

# Bienvenido a mi página de asignaciones

<ul>
  {% for post in site.posts %}
    <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


