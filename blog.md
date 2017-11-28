---
title: Blog
---

{% for post in site.posts %}

[{{post.title}}]({{post.url}})
------------------------------

<p class="post-date">{{post.date | date_to_long_string}}</p>

{% assign more = ' [<a href="' | append: {{post.url}} | append: '">read&nbsp;more…</a>]' %}
{{post.content | markdownify | strip_html | truncatewords: 50 | append: more}}

{{post.excerpt | markdownify | strip_html | append: more}}

<!-- {{post.excerpt | append: '[read more…]' | strip_newlines | markdownify | strip_html}} -->

<!-- [{{post.title}}]({{post.url}}) -->
<!-- ------------------------------ -->

<!-- <p class="post-date">{{post.date | date_to_long_string}}</p> -->

<!-- {{post.excerpt}} -->

<!-- [[read more…]({{post.url}})] -->

{% endfor %}
