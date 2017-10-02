---
title: Papers test
---

{% for paper in site.data.papers %}
  {{paper.author}}
  {{paper.title}}
{% endfor %}
