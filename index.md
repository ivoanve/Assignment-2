---
title: Ivonne's Assignment Portfolio
layout: home
---

# 👩‍🚀 Welcome to My Assignment Portfolio

Here you will find a collection of my 4 main assignments for the course.  
Each assignment is presented as a blog post below.

---

<ul>
  {% for post in site.posts %}
    <li>
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
    </li>
  {% endfor %}
</ul>
