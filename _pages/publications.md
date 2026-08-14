---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<div class="publications">

{% capture publication_list %}
{% bibliography %}
{% endcapture %}
{{ publication_list | regex_replace: '<a href="https://doi\.org/[^"]+"[^>]*>DOI</a>', '' }}

</div>
