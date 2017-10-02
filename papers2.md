---
title: Papers test
---

{% for paper in site.data.papers %}

{% for author in paper.authors %}{{author}},{% endfor %}
{{paper.title}}

{% endfor %}
