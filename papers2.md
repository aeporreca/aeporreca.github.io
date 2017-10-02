---
title: Papers test
---

{% for paper in site.data.papers %}
1. {% for author in paper.authors %}{{author}}, {% endfor %} [{{paper.title}}]({{paper.url}}). In *{{paper.publication}}* {{paper.volume}}, pages {{paper.pages}}, {{paper.year}}. [[preprint](/papers/{{paper.preprint}})]
{% endfor %}
