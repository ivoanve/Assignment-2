---
layout: default
title: Assignment Portfolio
---

<style>
  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
    color: #111;
    background: #fff;
    margin: 2rem auto;
    max-width: 600px;
    line-height: 1.6;
  }
  h1, h2 {
    font-weight: 600;
    color: #222;
    margin-bottom: 1rem;
  }
  hr {
    border: none;
    border-top: 1px solid #eee;
    margin: 2rem 0;
  }
  a {
    color: #0366d6;
    text-decoration: none;
  }
  a:hover {
    text-decoration: underline;
  }
  ul {
    padding-left: 1rem;
    list-style-type: none;
  }
  li {
    margin-bottom: 1rem;
  }
  small {
    color: #666;
  }
  .date {
    font-size: 0.9rem;
    color: #999;
  }
</style>

# 🎓 Ivonne's Academic Assignment Portfolio

Welcome to my academic portfolio. Here you will find a curated collection of my key assignments, developed throughout the course. Each one reflects different competencies, structured thinking, and analytical skills.

---

## 📁 Featured Assignments

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">📄 {{ post.title }}</a><br>
      <small class="date">📅 {{ post.date | date: "%B %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>

---

## 📝 About This Page

This page was created as part of a course assignment to demonstrate web publishing using **GitHub Pages** and **Markdown**. The content is organized to ensure easy navigation, clarity, and academic presentation.

---

## 📬 Contact

For inquiries or feedback, feel free to reach out:  
📧 ivoanve@ejemplo.com

---

<small>© 2025 Ivonne Anave. All rights reserved.</small>



