---
layout: single
title: Weekly Reading Group
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
    <i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }}
	{% if post.time %} @ {{post.time}} {% endif %} </b>
	<br>
    {{ post.content }}
    </div>
  {% endif %}
  {% endfor %}
  
  </section>

## Past Meetings

<section class="page__content cf">

{% assign i = 0 %}
{% assign curDate = site.time | date: '%s' %}
{% for post in site.posts %}
  {% assign postStartDate = post.date | date: '%s' %}
  {% if post.categories contains "seminar" and postStartDate < curDate and i < 9 %}
    <div class="news">
    <i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> <br>
    {{ post.content }}
    </div>
    {% assign i = i | plus:1 %}
  {% endif %}
{% endfor %}

</section>

<details>
<summary>Show all reading group meetings</summary>
<section class="page__content cf">
<br>
{% assign i = 0 %}
{% assign curDate = site.time | date: '%s' %}
{% for post in site.posts %}
  {% assign postStartDate = post.date | date: '%s' %}
  {% if post.categories contains "seminar" and postStartDate < curDate %}
    {% if i >= 9 %}
     <div class="news">
     <i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> <br>
      {{ post.content }}
    </div>
	{% endif %}
    {% assign i = i | plus:1 %}
  {% endif %}
{% endfor %}
</section>
</details>
 
