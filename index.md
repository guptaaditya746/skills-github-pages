---
layout: home
title: Welcome to my blog
---

# Welcome to my blog

Hi! This is a sample homepage for your Markdown-powered blog.

## Recent Posts

<ul>
  {% for post in site.posts limit:5 %}
    <li>
      <h3>
        <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </h3>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>
