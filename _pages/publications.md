---
layout: page
permalink: /publications/
title: Publications
description: publications by categories in reversed chronological order.
nav: true
nav_order: 3
---

<!-- _pages/publications.md -->

<style>
h2.bibliography {
  color: #999 !important;
}
[data-theme="dark"] h2.bibliography {
  color: #bbb !important;
}
[data-theme="dark"] .az-under-review {
  background: #fb923c !important;
  color: #fff !important;
}
</style>

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

<p style="font-size: 0.85rem; color: #888; margin: 0.5rem 0 0;"><em><sup>*</sup> denotes equal contribution</em></p>

{% if site.data.coming_soon.size > 0 %}
<h2 class="bibliography">Coming Soon</h2>
{% include coming_soon_papers.liquid %}
{% endif %}

{% bibliography %}

</div>
