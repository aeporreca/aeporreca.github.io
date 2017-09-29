---
title: Blog
---

{% for post in site.posts %}
1. [{{post.title}}]({{post.url}}), {{post.date | date_to_long_string}}

{% endfor %}

<!-- <ol> -->
<!-- {% for post in site.posts %} -->
<!-- <li><a href="{{post.url}}">{{post.title}}</a>, {{post.date | date_to_long_string}}</li> -->
<!-- {% endfor %} -->
<!-- </ol> -->
