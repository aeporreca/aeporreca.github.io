---
title: Blog
---

<!-- {% for post in site.posts %} -->
<!-- 1. [{{post.title}}]({{post.url}}), {{post.date | date_to_long_string}} -->

<!-- {% endfor %} -->

{% for post in site.posts %}
[{{post.title}}]({{post.url}})
------------------------------
<p id="post-date">{{post.date | date_to_long_string}}</p>
{{post.excerpt}}
[[read more…]({{post.url}})]
{% endfor %}
