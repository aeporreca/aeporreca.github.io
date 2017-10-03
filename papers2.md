---
title: Papers
---

This is a list of my [journal](#journal-papers) and [conference](#conference-and-workshop-papers) papers, as well as [book chapters](#book-chapters), [technical reports](#technical-reports), and [volumes](#volumes-edited) edited by me. Click on the title to reach the publisher’s website, or download a preprint if you do not have access to the published version of the paper.

Journal papers
--------------

{% for paper in data.journals  %}
1. {% include paper.html %}
{% endfor %}

<!-- Conference papers -->
<!-- ----------------- -->

<!-- {% assign conferences = site.data.papers2 | where: "type", "conference" %} -->
<!-- {% for paper in conferences  %} -->
<!-- 1. {% include format-conference.html %} -->
<!-- {% endfor %} -->

<!-- Book chapters -->
<!-- ------------- -->

<!-- {% assign chapters = site.data.papers2 | where: "type", "chapter" %} -->
<!-- {% for paper in chapters  %} -->
<!-- 1. {% include format-chapter.html %} -->
<!-- {% endfor %} -->

<!-- <\!-- {% assign chapters = site.data.papers -\-> -->
<!-- <\!--                    | where: 'type', 'chapter' -\-> -->
<!-- <\!--                    | sort: 'year' | reverse %} -\-> -->
<!-- <\!-- {% for paper in chapters %} -\-> -->
<!-- <\!-- 1. {% include paper.html %} -\-> -->
<!-- <\!-- {% endfor %} -\-> -->

<!-- <\!-- Technical reports -\-> -->
<!-- <\!-- ----------------- -\-> -->

<!-- <\!-- The papers in this section only include those that do not possess an extended version published in a peer-reviewed journal or conference. -\-> -->

<!-- <\!-- {% assign techreports = site.data.papers -\-> -->
<!-- <\!--                       | where: 'type', 'techreport' -\-> -->
<!-- <\!--                       | sort: 'year' | reverse %} -\-> -->
<!-- <\!-- {% for paper in reports %} -\-> -->
<!-- <\!-- 1. {% include paper.html %} -\-> -->
<!-- <\!-- {% endfor %} -\-> -->

<!-- <\!-- Volumes edited -\-> -->
<!-- <\!-- -------------- -\-> -->

<!-- <\!-- {% assign volumes = site.data.papers -\-> -->
<!-- <\!--                   | where: 'type', 'volume' -\-> -->
<!-- <\!--                   | sort: 'year' | reverse %} -\-> -->
<!-- <\!-- {% for paper in volumes %} -\-> -->
<!-- <\!-- 1. {% include paper.html %} -\-> -->
<!-- <\!-- {% endfor %} -\-> -->
