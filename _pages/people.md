---
title: People
layout: single
permalink: /people/
collection: people
author_profile: false
entries_layout: grid
classes: wide
sort_by: title
sort_order: forward
<!-- show_excerpts: true -->
---

This is the people page.

<section class="page__content cf">
<div class="entries-{{ entries_layout }}">
  {% include people-list.html collection=page.collection sort_by=page.sort_by sort_order=page.sort_order type=page.entries_layout %}
</div>
</section>
