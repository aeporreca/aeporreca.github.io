---
title: Blog
---

{% for post in site.posts %}

[{{post.title}}]({{post.url}})
------------------------------

<p class="post-date">{{post.date | date_to_long_string}}</p>

{% assign more = ' [<a href="' | append: {{post.url}}
    | append: '">read&nbsp;more…</a>]' %}
{{post.excerpt | markdownify | strip_newlines
    | remove: '<p>' | remove: '</p>' | append: more}}

{% endfor %}
