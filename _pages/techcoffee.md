---
layout: single
title: Technical Coffee
permalink: /techcoffee/
author_profile: false
---

The technical coffee is held every two weeks on a rotational basis over the groups' members and lasts around 90 minutes. Pen and paper or whiteboard presentations instead of slides are preferred, encouraging a slower-paced and interactive format with plenty of questions and constructive, yet critical feedback. The sessions focus on technical or mathematical aspects of our members' ongoing research projects.

<h2>Upcoming</h2>

<section class="page__content cf">

{% capture curDate %}{{ site.time | date: '%F' }}{% endcapture %}
{% for post in site.posts %}
  {% capture postStartDate %}{{ post.date | date: '%F' }}{% endcapture %}
  {% if post.categories contains "coffee" and postStartDate >= curDate %}
    <div class="news">
    <b class="news-title"> <i class="fas {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b>
	{% if post.time %} @ {{post.time}} {% endif %} </b>
	<br>
    {{ post.content }}
    </div>
  {% endif %}
  {% endfor %}
  
  </section>

<h2>Past Meetings</h2>

<section class="page__content cf">

{% assign i = 0 %}
{% capture curDate %}{{ site.time | date: '%F' }}{% endcapture %}
{% for post in site.posts %}
  {% capture postStartDate %}{{ post.date | date: '%F' }}{% endcapture %}
  {% if post.categories contains "coffee" and postStartDate < curDate and i < 9 %}
    <div class="news">
    <b class="news-title"> <i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> </b> <br>
    {{ post.content }}
    </div>
    {% assign i = i | plus:1 %}
  {% endif %}
{% endfor %}

</section>

<details>
<summary>Show all technical coffee meetings</summary>
<section class="page__content cf">
<br>
{% assign i = 0 %}
{% capture curDate %}{{ site.time | date: '%F' }}{% endcapture %}
{% for post in site.posts %}
  {% capture postStartDate %}{{ post.date | date: '%F' }}{% endcapture %}
  {% if post.categories contains "coffee" and postStartDate < curDate %}
    {% if i >= 9 %}
     <div class="news">
      <b class="news-title"> <i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> </b> <br>
      {{ post.content }}
    </div>
	{% endif %}
    {% assign i = i | plus:1 %}
  {% endif %}
{% endfor %}
</section>
</details>
 
