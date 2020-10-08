---
title: Current Team Members
layout: single
permalink: /people/
affiliation_profile: false
entries_layout: grid
custom_css: people
<!-- classes: wide -->
<!-- show_excerpts: true -->
---

<section class="page__content cf">
<div class="entries-{{ entries_layout }}">
  {% assign members = site.people | where: 'type', 'member' %}
  {% assign groups = members | group_by: 'rank' | sort: 'name' %}
  {% for group in groups %}
    {% assign entriesInGroup = group.items | sort: 'date' %}
    {% for post in entriesInGroup %}
      {% include people-single.html type=page.entries_layout %}
    {%- endfor -%}
  {% endfor %}
</div>
</section>

<section class="page__content cf">
<h1>Alumni</h1>
<h3>Postdocs</h3>
<table class="responsive-table table">
  <tr>
    <th>Name</th>
    <th>Dates</th>
  </tr>
  {% assign alumni = site.people | where: 'type', 'alumni' %}
  {% for post in alumni %}
    {% if post.rank == 3 %}
      <tr>
        <td>{{ post.title }}</td>
        <td>{{ post.date | date: '%m/%y' }}-{{ post.date_leave | date: '%m/%y' }}</td>
      </tr>
    {% endif %}
  {% endfor %}
</table>
<br>
<!--  -->
<h3>Research Assistants</h3>
<table class="responsive-table table">
  <tr>
    <th>Name</th>
    <th>Dates</th>
  </tr>
  {% assign alumni = site.people | where: 'type', 'alumni' %}
  {% for post in alumni %}
    {% if post.rank == 5 %}
      <tr>
        <td>{{ post.title }}</td>
        <td>{{ post.date | date: '%m/%y' }}-{{ post.date_leave | date: '%m/%y' }}</td>
      </tr>
    {% endif %}
  {% endfor %}
</table>
<br>
<!--  -->
<h3>Interns / Trainees</h3>
<table class="responsive-table table">
  <tr>
    <th>Name</th>
    <th>Dates</th>
    <th>Affliation</th>
  </tr>
  {% assign alumni = site.people | where: 'type', 'alumni' %}
  {% for post in alumni %}
    {% if post.rank == 7 %}
      <tr>
        <td>{{ post.title }}</td>
        <td>{{ post.date | date: '%m/%y' }}-{{ post.date_leave | date: '%m/%y' }}</td>
        <td>{{post.affliation}}</td>
      </tr>
    {% endif %}
  {% endfor %}
</table>
</section>
