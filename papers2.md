---
title: Papers
---

This is a list of my [journal](#journal-papers) and [conference](#conference-and-workshop-papers) papers, as well as [book chapters](#book-chapters), [technical reports](#technical-reports), and [volumes](#volumes-edited) edited by me. Click on the title to reach the publisher’s website, or download a preprint if you do not have access to the published version of the paper.

Journal papers
--------------

{% assign journals = site.data.papers | where:'type','journal' | sort: 'author' | sort: 'year' %}
{% for paper in journals %}
1. {% include paper.html %}
{% endfor %}

Conference papers
-----------------

{% assign conferences = site.data.papers | where:'type','conference' %}
{% for paper in conferences %}
1. {% include paper.html %}
{% endfor %}

Book chapters
-------------

{% assign chapters = site.data.papers | where:'type','chapter' %}
{% for paper in chapters %}
1. {% include paper.html %}
{% endfor %}

Technical reports
-----------------

{% assign reports = site.data.papers | where:'type','techreport' %}
{% for paper in reports %}
1. {% include paper.html %}
{% endfor %}

Volumes edited
--------------

{% assign volumes = site.data.papers | where:'type','volume' %}
{% for paper in volumes %}
1. {% include paper.html %}
{% endfor %}
