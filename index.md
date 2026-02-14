---
layout: default
title: Home
---

# Hello.

I am a developer and writer. This acts as my digital garden—a collection of thoughts, code snippets, and essays.

## Featured Projects

<div class="project-grid">
  {% for post in site.posts %}
    {% if post.category == 'project' %}
      <a href="{{ post.url }}" class="project-card">
        <h3>{{ post.title }}</h3>
        <p>{{ post.description }}</p>
      </a>
    {% endif %}
  {% endfor %}
</div>

<hr style="margin: 3rem 0; border: 0; border-top: 1px solid rgba(0,0,0,0.1);">

## Latest Writings

<ul class="post-list">
  {% for post in site.posts %}
    {% if post.category == 'essay' %}
    <li>
      <span class="post-meta">{{ post.date | date: "%b %d, %Y" }}</span>
      <h3>
        <a class="post-link" href="{{ post.url }}">{{ post.title }}</a>
      </h3>
    </li>
    {% endif %}
  {% endfor %}
</ul>

---

### Contact
You can find me on [GitHub](https://github.com/shivanshsharma8834) or email me at `hello@example.com`.