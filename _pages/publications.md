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

{% bibliography %}

</div>
