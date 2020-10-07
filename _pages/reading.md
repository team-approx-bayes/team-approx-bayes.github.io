---
layout: single
title: Reading Group
permalink: /reading/
author_profile: false
---

## Upcoming

<section class="page__content cf">

{% assign curDate = site.time | date: '%s' %}
{% for post in site.posts %}
  {% assign postStartDate = post.date | date: '%s' %}
  {% if post.categories contains "seminar" and postStartDate >= curDate %}
    <div class="news">
    <i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} @ {{post.time}} </b>
	<br>
    {{ post.content }}
    </div>
  {% endif %}
  {% endfor %}
  
</section>
  

## Past Meetings

<section class="page__content cf">

{% assign curDate = site.time | date: '%s' %}
{% for post in site.posts %}
  {% assign postStartDate = post.date | date: '%s' %}
  {% if post.categories contains "seminar" and postStartDate < curDate %}
    <div class="news">
    <i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> <br>
    {{ post.content }}
    </div>
  {% endif %}
{% endfor %}

</section>
