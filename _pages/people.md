---
title: Current team members
layout: single
permalink: /people/
author_profile: false
entries_layout: grid
<!-- classes: wide -->
<!-- show_excerpts: true -->
---

<section class="page__content cf">
<div class="entries-{{ entries_layout }}">
  {% assign groups = site['people'] | group_by: 'rank' | sort: 'name' %}
  {% for group in groups %}
    {% assign entriesInGroup = group.items | sort: 'date' %}
    {% for post in entriesInGroup %}
      {% include people-single.html type=page.entries_layout %}
    {%- endfor -%}
  {% endfor %}
</div>
</section>
