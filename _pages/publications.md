Description
Journal articles, book chapters, and conference proceedings in reverse chronological order.

Layout
page

Permalink
/publications/

Title
publications

Nav
true

Nav_order
2

<!-- _pages/publications.md -->
{% include bib_search.liquid %}

<div class="publications">
{% capture inpress_html %}{% bibliography --group_by none --query @*[status=inpress] %}{% endcapture %} {% if inpress_html contains '<li' %}

<h2 class="bibliography">in press</h2> {{ inpress_html }} {% endif %}
{% bibliography --query @*[status!=inpress] %}

</div>
