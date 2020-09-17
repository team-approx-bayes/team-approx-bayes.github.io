---
title: Current team members
layout: single
permalink: /people/
collection: people
author_profile: false
entries_layout: grid
sort_by: title
sort_order: forward
<!-- classes: wide -->
<!-- show_excerpts: true -->
---

<section class="page__content cf">
<div class="entries-{{ entries_layout }}">
  {% include people-list.html collection=page.collection sort_by=page.sort_by sort_order=page.sort_order type=page.entries_layout %}
</div>
</section>
