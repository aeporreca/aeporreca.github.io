---
title: Blog
---

{% for post in site.posts %}

[{{post.title}}]({{post.url}})
------------------------------

<p class="post-date">{{post.date | date_to_long_string}}</p>

{{post.excerpt | strip_newlines | append: '[read more…]' | strip_newlines}}

{{post.excerpt | strip_newlines | append: '[read more…]' | strip_newlines | strip_newlines}}

<!-- {{post.excerpt | append: '[read more…]' | strip_newlines | markdownify | strip_html}} -->

<!-- [{{post.title}}]({{post.url}}) -->
<!-- ------------------------------ -->

<!-- <p class="post-date">{{post.date | date_to_long_string}}</p> -->

<!-- {{post.excerpt}} -->

<!-- [[read more…]({{post.url}})] -->

{% endfor %}
