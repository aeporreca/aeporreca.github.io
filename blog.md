---
title: Blog
---

{% for post in site.posts %}

[{{post.title}}]({{post.url}})
------------------------------

<p id="post-date">{{post.date | date_to_long_string}}</p>

{% assign paragraphs = post.content | newline_to_br | split: '<br />' %}
<!-- {{post.excerpt | append: '[read more…]' | strip_newlines | markdownify | strip_html}} -->
<!-- {{post.excerpt | append: '[read more…]' | strip_newlines}} -->
{{post.paragraphs[1] | append: '[read more…]'}}

<!-- [{{post.title}}]({{post.url}}) -->
<!-- ------------------------------ -->

<!-- <p id="post-date">{{post.date | date_to_long_string}}</p> -->

<!-- {{post.excerpt}} -->

<!-- [[read more…]({{post.url}})] -->

{% endfor %}
