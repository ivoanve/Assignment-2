---
layout: default
title: Assignment Portfolio
---

<style>
  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
    color: #2c3e50;
    background: #f9fafb;
    margin: 2rem auto;
    max-width: 640px;
    line-height: 1.7;
    padding: 0 1rem;
  }
  h1, h2 {
    font-weight: 700;
    color: #1a73e8; /* Azul vibrante */
    margin-bottom: 1rem;
  }
  hr {
    border: none;
    border-top: 2px solid #e0e7ff; /* azul pastel */
    margin: 2rem 0;
  }
  a {
    color: #1a73e8;
    text-decoration: none;
    transition: color 0.3s ease;
  }
  a:hover {
    color: #0049b7;
    text-decoration: underline;
  }
  ul {
    padding-left: 0;
    list-style-type: none;
  }
  li {
    background: #ffffff;
    box-shadow: 0 1px 4px rgb(0 0 0 / 0.05);
    padding: 1rem 1.2rem;
    margin-bottom: 1rem;
    border-radius: 6px;
    transition: box-shadow 0.2s ease;
  }
  li:hover {
    box-shadow: 0 4px 12px rgb(0 0 0 / 0.1);
  }
  small.date {
    font-size: 0.9rem;
    color: #5a6d8c; /* Azul grisáceo */
  }
  small.footer {
    display: block;
    margin-top: 3rem;
    font-size: 0.8rem;
    color: #7a8ba6;
    text-align: center;
  }
  .contact {
    margin-top: 2rem;
    font-size: 1rem;
    color: #34495e;
  }
</style>

# 🎓 Academic Assignments Portfolio

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

<div class="contact">
For inquiries or feedback, feel free to reach out:<br>  
📧 ivoanve@ejemplo.com
</div>

---

<small class="footer">© 2025 Ivonne Anave. All rights reserved.</small>

