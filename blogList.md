---
title: "Blog list"
layout: page
permalink: "/bloggers/"
---

{% for blog in site.data.blogList %}
  {{ blog.name }}: {{ blog.url }}
{% endfor %}