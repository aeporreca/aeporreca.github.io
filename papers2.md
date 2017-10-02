---
title: Papers
---

This is a list of my [journal](#journal-papers) and [conference](#conference-and-workshop-papers) papers, as well as [book chapters](#book-chapters), [technical reports](#technical-reports), and [volumes](#volumes-edited) edited by me. Click on the title to reach the publisher’s website, or download a preprint if you do not have access to the published version of the paper.

{% for paper in site.data.papers %}
1. {% include paper.html %}
{% endfor %}
