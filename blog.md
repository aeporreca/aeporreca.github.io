---
title: Blog
---

<ol>
{% for post in site.posts %}
<li><p><a href="{{post.url}}">{{post.title}}</a>, {{post.date | date_to_long_string}}</li></p>
{% endfor %}
</ol>
