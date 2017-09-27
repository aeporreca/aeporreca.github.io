---
title: Blog
---

{% for post in site.posts %}
1. [{{post.title}}]({{post.url}})
{% endfor %}
