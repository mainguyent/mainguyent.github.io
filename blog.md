---
layout: default
title: Blog
permalink: /blog/
---

# Blog

Notes, write-ups, and things I find worth sharing.

---

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url }})

<small>{{ post.date | date: "%B %-d, %Y" }}</small>

{{ post.excerpt }}

---
{% endfor %}

{% if site.posts.size == 0 %}
*No posts yet — check back soon.*
{% endif %}
