---
layout: page
permalink: /publications/
title: publications
nav: true
nav_order: 1
bibliography_types:
  - id: article
    title: Journal Articles
  - id: inproceedings
    title: Conference Papers
---
<!-- _pages/publications.md -->
<div class="publications">

{% for type in page.bibliography_types %}
  <h2>{{ type.title }}</h2>
  {% bibliography -f papers -q @*[entrytype={{ type.id }}]* %}
{% endfor %}

</div>

