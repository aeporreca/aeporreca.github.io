---
title: Papers test
---

{% for paper in site.data.papers %}
  {% for x in paper.author %}
    {{x}}
  {% endfor %}
  {{paper.author}}
  {{paper.title}}
{% endfor %}
