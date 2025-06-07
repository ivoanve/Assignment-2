---
layout: Software 
title: Home
---

# Assignments

Here are the available assignments:

<ul>
  {% for post in site.posts %}
    <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


