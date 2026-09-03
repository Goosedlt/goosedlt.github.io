---
layout: page
title: Blog
icon: fas fa-camera
order: 2
---

## Latest Stuff

<ul>
  {% for post in site.categories.Blog %}
    <li>
      <span>{{ post.date | date: "%b %d, %Y" }}</span> &raquo; 
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
