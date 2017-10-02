---
title: Papers
---

This is a list of my [journal](#journal-papers) and [conference](#conference-and-workshop-papers) papers, as well as [book chapters](#book-chapters), [technical reports](#technical-reports), and [volumes](#volumes-edited) edited by me. Click on the title to reach the publisher’s website, or download a preprint if you do not have access to the published version of the paper.

Journal papers
--------------

{% for paper in site.data.papers %}
{% include paper.html %}
{% endfor %}

<!-- Conference and workshop papers -->
<!-- ------------------------------ -->

<!-- {% for paper in site.data.papers %} -->
<!-- {% if paper.type = "conference-paper" %} -->
<!-- {% include paper.html %} -->
<!-- {% endif %} -->
<!-- {% endfor %} -->

<!-- <\!-- {% for paper in site.data.conference-papers %} -\-> -->
<!-- <\!-- {% include paper.html %} -\-> -->
<!-- <\!-- {% endfor %} -\-> -->

<!-- Book chapters -->
<!-- ------------- -->

<!-- {% for paper in site.data.papers %} -->
<!-- {% if paper.type = "book-chapter" %} -->
<!-- {% include paper.html %} -->
<!-- {% endif %} -->
<!-- {% endfor %} -->

<!-- <\!-- {% for paper in site.data.book-chapters %} -\-> -->
<!-- <\!-- {% include paper.html %} -\-> -->
<!-- <\!-- {% endfor %} -\-> -->

<!-- Technical reports -->
<!-- ----------------- -->

<!-- The papers in this section only include those that do not possess an extended version published in a peer-reviewed journal or conference. -->

<!-- {% for paper in site.data.papers %} -->
<!-- {% if paper.type = "technical-report" %} -->
<!-- {% include paper.html %} -->
<!-- {% endif %} -->
<!-- {% endfor %} -->

<!-- <\!-- {% for paper in site.data.technical-reports %} -\-> -->
<!-- <\!-- {% include paper.html %} -\-> -->
<!-- <\!-- {% endfor %} -\-> -->

<!-- Volumes edited -->
<!-- -------------- -->

<!-- {% for paper in site.data.papers %} -->
<!-- {% if paper.type = "edited-volume" %} -->
<!-- {% include paper.html %} -->
<!-- {% endif %} -->
<!-- {% endfor %} -->

<!-- <\!-- {% for paper in site.data.volumes-edited %} -\-> -->
<!-- <\!-- {% include paper.html %} -\-> -->
<!-- <\!-- {% endfor %} -\-> -->
