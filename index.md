---
layout: default
title: Assignments Portfolio
---

<style>
  /* Variables para colores y fuentes */
  :root {
    --color-primary: #1a73e8;
    --color-primary-dark: #0049b7;
    --color-bg: #f9fafb;
    --color-text: #2c3e50;
    --color-muted: #5a6d8c;
    --font-base: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap');

  body {
    font-family: var(--font-base);
    color: var(--color-text);
    background: var(--color-bg);
    margin: 2rem auto;
    max-width: 640px;
    line-height: 1.7;
    padding: 0 1rem;
  }

  h1, h2 {
    font-weight: 700;
    color: var(--color-primary);
    margin-bottom: 1rem;
  }

  hr {
    border: none;
    border-top: 2px solid #e0e7ff;
    margin: 2rem 0;
  }

  a {
    color: var(--color-primary);
    text-decoration: none;
    transition: color 0.3s ease;
  }

  a:hover {
    color: var(--color-primary-dark);
    text-decoration: underline;
  }

  ul {
    padding-left: 0;
    list-style-type: none;
  }

  li {
    background: #fff;
    box-shadow: 0 1px 4px rgb(0 0 0 / 0.05);
    padding: 1.2rem 1.5rem;
    margin-bottom: 1rem;
    border-radius: 8px;
    transition: box-shadow 0.3s ease, transform 0.2s ease;
    cursor: pointer;
  }

  li:hover {
    box-shadow: 0 6px 16px rgb(0 0 0 / 0.12);
    transform: translateY(-4px);
  }

  small.date {
    font-size: 0.9rem;
    color: var(--color-muted);
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

  /* Responsive para móviles */
  @media (max-width: 480px) {
    body {
      margin: 1rem;
      padding: 0 0.5rem;
    }
    h1 {
      font-size: 1.6rem;
    }
    h2 {
      font-size: 1.3rem;
    }
    li {
      padding: 1rem;
    }
  }
</style>

# 🎓 Academic Assignments Portfolio

Welcome to my academic portfolio. Here you will find a curated collection of my key assignments, developed throughout the course. Each one reflects different competencies, structured thinking, and analytical skills.

---

## 📁 Featured Assignments

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ site.baseurl }}{{ post.url }}">📄 {{ post.title }}</a><br>
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
📧 ivonne.anavez@gmail.com
</div>

---

<small class="footer">© 2025 Ivonne Anave. All rights reserved.</small>
