---
layout: default
title: Assignment Portfolio
---
<link rel="stylesheet" href="assets/style.css">

# 🎓 Ivonne's Academic Assignment Portfolio

Welcome to my academic portfolio. Here you will find a curated collection of my key assignments, developed throughout the course. Each one reflects different competencies, structured thinking, and analytical skills.

---

## 📁 Featured Assignments

<ul style="list-style: none; padding-left: 0;">
  {% for post in site.posts %}
    <li style="margin-bottom: 1rem;">
      <a href="{{ post.url }}" style="font-weight: bold; font-size: 1.1rem;">
        📄 {{ post.title }}
      </a><br>
      <small style="color: gray;">📅 {{ post.date | date: "%B %d, %Y" }}</small>
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


