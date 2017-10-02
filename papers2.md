---
title: Papers test
---

{% for paper in site.data.papers %}
  {% for x in paper.authors %}
    {{x}}
  {% endfor %}
  {{paper.title}}
{% endfor %}
