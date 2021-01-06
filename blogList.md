---
title: "Blog list"
layout: page
permalink: "/bloggers/"
---

{% for blog in site.data.blogList %}
  {{ blog.username }}: {{ blog.url }}
{% endfor %}