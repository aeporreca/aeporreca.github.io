---
title: Papers test
---

{% for paper in site.data.papers %}
{% for author in paper.authors %}
{{author.given}} {{author.family}}, 
{% endfor %}
[{{paper.title}}](paper.url).
In
{% for editor in paper.editors %}
{{editor.given}} {{editor.family}}
{% if forloop.last == true %}
(eds.)
{% endif %},
{% endfor %}
{{paper.publication}}
{% if paper.series %}
volume {{paper.volume}} of {{paper.series}}
{% elsif paper.volume %}
{{paper.volume}}
{% endif %}
{% if paper.publisher %}
, {{paper.publisher}}
{% endif %}
{% if paper.year %}
, {{paper.year}}
{% endif %}
{% if paper.preprint %}
[[preprint](/papers/{{paper.preprint}})]
{% endif %}
{% endfor %}

<!-- {% for paper in site.data.papers %} -->
<!-- 1. {% for author in paper.authors %}{{author.given}} {{author.family}}, {% endfor %}[{{paper.title}}]({{paper.url}}).{% if paper.publication %} In {% if paper.editors %}{% endif %} *{{paper.publication}}*{% endif %}{% if paper.volume %} {{paper.volume}}{% endif %}{% if paper.pages %}, pages {{paper.pages}}{% endif %}{% if paper.year %}, {{paper.year}}{% endif %}{% if paper.preprint %} [[preprint](/papers/{{paper.preprint}})]{% endif %} -->
<!-- {% endfor %} -->
