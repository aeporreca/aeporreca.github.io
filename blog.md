---
title: Blog
---

{% for post in site.posts %}

[{{post.title}}]({{post.url}})
------------------------------

<p class="post-date">{{post.date | date_to_long_string}}</p>
{% assign more = '[read more…]' %}
{{post.content | markdownify | strip_html | truncatewords: 50 | append: more}}

<!-- {{post.excerpt | append: '[read more…]' | strip_newlines | markdownify | strip_html}} -->

<!-- [{{post.title}}]({{post.url}}) -->
<!-- ------------------------------ -->

<!-- <p class="post-date">{{post.date | date_to_long_string}}</p> -->

<!-- {{post.excerpt}} -->

<!-- [[read more…]({{post.url}})] -->

{% endfor %}
