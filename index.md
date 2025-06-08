---
layout: default
title: Assignment Portfolio
---

# 📚 Ivonne's Assignment Portfolio

Welcome to my assignment portfolio. Below you will find my 4 key assignments presented as blog posts.

---

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>  
      <small>📅 {{ post.date | date: "%B %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>


