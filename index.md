---
layout: home
title: Home
---

# Hello, I'm Parth

Welcome to my personal website. I build things and write about my experiences.

## Recent Posts

{% for post in site.posts limit:5 %}
- [{{ post.title }}]({{ post.url | relative_url }})
  {{ post.date | date: "%B %-d, %Y" }}
{% endfor %}

---

[View all posts →]({{ "/blog" | relative_url }}) · [My Projects →]({{ "/projects" | relative_url }})
