---
title: Papers test
---

<!-- {% for paper in site.data.papers %} -->
<!-- {% for author in paper.authors %}{{author.given}} {{author.family}}, {% endfor %}[{{paper.title}}](paper.url){% if paper.editors %}, in{% endif %}{% for editor in paper.editors %} {{editor.given}} {{editor.family}}{% if forloop.last == true %} (editors){% else %},{% endif %}{% endfor %}{% if paper.publication %}, *{{paper.publication}}*{% endif %}{% if paper.series %}, volume {{paper.volume}} of {{paper.series}}{% elsif paper.volume %} {{paper.volume}}{% endif %}{% if paper.publisher %}, {{paper.publisher}}{% endif %}{% if paper.year %}, {{paper.year}}{% endif %}{% if paper.preprint %} [[preprint](/papers/{{paper.preprint}})]{% endif %} -->
<!-- {% endfor %} -->

{% for paper in site.data.papers %}
{% include paper.html parameter=paper %}
{% endfor %}
