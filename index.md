---
layout: home
title: Home
---

# Welcome to My Blog

## Latest Post
{% assign latest = site.posts.first %}
### [{{ latest.title }}]({{ latest.url }})
{{ latest.excerpt }}

---

## Recent Posts
<ul>
  {% for post in site.posts offset:1 limit:2 %}
    <li>
      <h4><a href="{{ post.url }}">{{ post.title }}</a></h4>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>

[See All Posts →](/archive)
