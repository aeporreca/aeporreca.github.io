---
title: Papers
---

This is a list of my [journal](#journal-papers) and [conference](#conference-and-workshop-papers) papers, as well as [book chapters](#book-chapters), [technical reports](#technical-reports), and [volumes](#volumes-edited) edited by me. Click on the title to reach the publisher’s website, or download a preprint if you do not have access to the published version of the paper.

Journal papers
--------------

{% for paper in site.data.journals %}
1. {% include paper.html %}
{% endfor %}

Conference papers
-----------------

{% for paper in site.data.conferences %}
1. {% include paper.html %}
{% endfor %}

Book chapters
-------------

{% for paper in site.data.chapters %}
1. {% include paper.html %}
{% endfor %}

Technical reports
-----------------

The papers in this section only include those that do not possess an extended version published in a peer-reviewed journal or conference.

{% for paper in site.data.techreports %}
1. {% include paper.html %}
{% endfor %}

Volumes edited
--------------

{% for paper in site.data.volumes %}
1. {% include paper.html %}
{% endfor %}
