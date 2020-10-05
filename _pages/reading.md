---
layout: single
title: Weekly Seminar / Reading Group
permalink: /seminar/
author_profile: false
---

## Upcoming

<section class="page__content cf">

{% assign curDate = site.time | date: '%s' %}
{% for post in site.posts %}
{% assign postStartDate = post.date | date: '%s' %}
{% if post.categories contains 'seminar' %}
    {% if postStartDate >= curDate %}
    <div class="news">
       <i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} @ {{post.time}} </b> <br>
      {{ post.content }}
    </div>
  {% endif %}
  {% endif %}
{% endfor %}

</section>

## Past Meetings

<section class="page__content cf">

{% assign curDate = site.time | date: '%s' %}
{% for post in site.posts %}
{% assign postStartDate = post.date | date: '%s' %}
  {% if postStartDate < curDate %}
  {% if post.categories contains 'seminar' %}
    <div class="news">
       <i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> <br>
      {{ post.content }}
    </div>
  {% endif %}
  {% endif %}
{% endfor %}

</section>










