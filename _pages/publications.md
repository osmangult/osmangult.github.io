---
layout: page
permalink: /publications/
title: publications
description: Journal articles, book chapters, conference proceedings, and theses in reverse chronological order.
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

{% include bib_search.liquid %}

<div class="publications">

<h1>Articles</h1>

{% capture inpress_html %}{% bibliography --group_by none --query @article[status=inpress] %}{% endcapture %}
{% if inpress_html contains '<li' %}
<h2 class="bibliography">in press</h2>
{{ inpress_html }}
{% endif %}

{% bibliography --query @article[status!=inpress] %}

<h1>Book Chapters</h1>

{% bibliography --query @incollection %}

<h1>Conference Proceedings</h1>

{% bibliography --query @inproceedings %}

<h1>Theses</h1>

{% bibliography --query @phdthesis,@mastersthesis %}

</div>
