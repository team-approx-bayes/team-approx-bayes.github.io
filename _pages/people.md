---
title: Current Team Members
layout: single
permalink: /people/
affiliation_profile: false
author_profile: false
entries_layout: grid
custom_css: people
<!-- classes: wide -->
<!-- show_excerpts: true -->
---

The Approximate Bayesian Inference Team is a diverse group of people that
encourages a multi-cultural environment. We think this is a key ingredient for any successful workplace,
even more so for research.
We are committed to establishing a welcoming environment for people of any
background, and as such we encourage applications from any minority.

If you are interested in joining us, please [check the news](../news/) for open positions or see
[here](../vacancies/) for available RIKEN programmes.

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
<h2>Research Scientists</h2>
<table class="responsive-table table">
  <tr>
    <th>Name</th>
    <th>Dates</th>
	<th>Next Destination</th>
  </tr>
  {% assign alumni = site.people | where: 'type', 'alumni' | sort: 'date' | reverse %}
  {% for post in alumni %}
    {% if post.rank == 2 %}
      <tr>
        <td>{{ post.title }}</td>
        <td>{{ post.date | date: '%m/%y' }}-{{ post.date_leave | date:'%m/%y' }}</td>
		<td>{{ post.wentto }}</td>
      </tr>
    {% endif %}
  {% endfor %}
</table>
<br>
<!--  -->

<h2>Postdoctoral Researcher</h2>
<table class="responsive-table table">
  <tr>
    <th>Name</th>
    <th>Dates</th>
	<th>Next Destination</th>
  </tr>
  {% assign alumni = site.people | where: 'type', 'alumni' | sort: 'date' | reverse %}
  {% for post in alumni %}
    {% if post.rank == 3 %}
      <tr>
        <td>{{ post.title }}</td>
        <td>{{ post.date | date: '%m/%y' }}-{{ post.date_leave | date: '%m/%y' }}</td>
        <td>{{ post.wentto }}</td>
      </tr>
    {% endif %}
  {% endfor %}
</table>
<p> * Special Postdoctoral Researcher <p>
<br>
<!--  -->
<h2>Research Assistants</h2>
<table class="responsive-table table">
  <tr>
    <th>Name</th>
    <th>Dates</th>
	<th>Next Destination</th>
  </tr>
  {% assign alumni = site.people | where: 'type', 'alumni' | sort: 'date' | reverse %}
  {% for post in alumni %}
    {% if post.rank == 5 %}
      <tr>
        <td>{{ post.title }}</td>
        <td>{{ post.date | date: '%m/%y' }}-{{ post.date_leave | date: '%m/%y' }}</td>
        <td>{{ post.wentto }}</td>
      </tr>
    {% endif %}
  {% endfor %}
</table>
<br>
<!--  -->
<h2>Interns / Trainees / Remote Collaborators / Rotation Students </h2>
<table class="responsive-table table" font-size="1em">
  <tr>
    <th>Name</th>
    <th>Dates</th>
    <th>Affliation</th>
    <th>Next Destination</th>
  </tr>
  {% assign alumni = site.people | where: 'type', 'alumni' | sort: 'date_leave' | reverse %}
  {% for post in alumni %}
    {% if post.rank == 7 %}
      <tr>
        <td>{{ post.title }}</td>
        <td>{{ post.date | date: '%m/%y' }}-{{ post.date_leave | date: '%m/%y' }}</td>
        <td>{{post.affliation}}</td>
        <td>{{post.wentto}}</td>
      </tr>
    {% endif %}
  {% endfor %}
</table>

<section>
<br>
<h1>Group Photos</h1>

<h2> Thomas's Promotion Party, March 2025 </h2>
<img src="../assets/images/group/thomas_promote.jpg" alt="team photo" width="450" height="600">

<br><br>

<h2> 2024 AIP Retreat, March 2025 </h2>
<div style="display: flex; align-items: flex-start; gap: 20px;">
  <img src="../assets/images/group/2024retreat_1.jpg" alt="team photo" width="450" height="600">
  <img src="../assets/images/group/2024retreat_2.jpg" alt="team photo" width="450" height="600">
</div>
