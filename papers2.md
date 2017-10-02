---
title: Papers test
---

{% for paper in site.data.papers %}
{% for author in paper.authors %}{{author.given}} {{author.family}}{% if forloop.last != true %},{% endif %}
{% endfor %}
{% endfor %}

<!-- {% for paper in site.data.papers %} -->
<!-- 1. {% for author in paper.authors %}{{author.given}} {{author.family}}, {% endfor %}[{{paper.title}}]({{paper.url}}).{% if paper.publication %} In {% if paper.editors %}{% endif %} *{{paper.publication}}*{% endif %}{% if paper.volume %} {{paper.volume}}{% endif %}{% if paper.pages %}, pages {{paper.pages}}{% endif %}{% if paper.year %}, {{paper.year}}{% endif %}{% if paper.preprint %} [[preprint](/papers/{{paper.preprint}})]{% endif %} -->
<!-- {% endfor %} -->
