---
title: Blog
---

{% for post in site.posts %}

[{{post.title}}]({{post.url}})
------------------------------

<p id="post-date">{{post.date | date_to_long_string}}</p>

{{post.excerpt | append: '[more]' | markdownify | strip_html}}

<!-- [{{post.title}}]({{post.url}}) -->
<!-- ------------------------------ -->

<!-- <p id="post-date">{{post.date | date_to_long_string}}</p> -->

<!-- {{post.excerpt}} -->

<!-- [[read more…]({{post.url}})] -->

{% endfor %}
