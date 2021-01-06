---
title: "Blog list"
layout: page
permalink: "/blogs/"
---

{% for blog in site.data.blogList %}
  {{ blog.name }}: {{ blog.url }}
{% endfor %}