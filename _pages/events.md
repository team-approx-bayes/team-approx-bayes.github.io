---
layout: single
title: Events
permalink: /events/
author_profile: false
---

Events for ABI Team:
<ul class="w3-ul">
  <li> <i class="fa fa-book" style="font-size: 25px;"></i> <strong><em>Reading Group</em></strong>: A group member takes the lead, presenting a chosen paper for discussion. </li>
  <li> <i class="fa fa-coffee" style="font-size: 25px;"></i> <em><strong>Tech Coffee</strong></em>: A full-time member takes the lead, discussing technical aspects of our members' ongoing research projects.</li>
  <li> <i class="fa fa-chalkboard-teacher" style="font-size: 25px;"></i> <em><strong>Seminar</strong></em>: We frequently invite external speakers to give talks or tutorials.</li>
  <li> <i class="fa fa-pizza-slice" style="font-size: 25px;"></i> <em><strong>Meta Meals</strong></em>: We hold guided discussions over lunch on research and more general topics.</li> 
</ul>	

<h2>Upcoming</h2>

<section class="page__content cf">

{% capture curDate %}{{ site.time | date: '%F' }}{% endcapture %}
{% for post in site.posts %}
  {% capture postStartDate %}{{ post.date | date: '%F' }}{% endcapture %}
  {% if post.categories contains "seminar" and postStartDate >= curDate %}
    <div class="news">
    <b class="news-title"> <i class="fa {{post.logo}}" style="font-size: 25px;"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b>
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
  {% if post.categories contains "seminar" and postStartDate < curDate and i < 9 %}
    <div class="news">
    <b class="news-title"> <i class="fa {{post.logo}}" style="font-size: 25px;"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> </b> <br>
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
{% capture curDate %}{{ site.time | date: '%F' }}{% endcapture %}
{% for post in site.posts %}
  {% capture postStartDate %}{{ post.date | date: '%F' }}{% endcapture %}
  {% if post.categories contains "seminar" and postStartDate < curDate %}
    {% if i >= 9 %}
     <div class="news">
      <b class="news-title"> <i class="fa {{post.logo}}" style="font-size: 25px;"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> </b> <br>
      {{ post.content }}
    </div>
	{% endif %}
    {% assign i = i | plus:1 %}
  {% endif %}
{% endfor %}
</section>
</details>
 
<!-- <br>
{% assign posts = site.posts | where: 'categories', 'lab-activities' | sort: 'date' | reverse %}
{% assign latest_post = posts.first %}
<div class="post">
      <h3>
      <a href="{{ latest_post.url | prepend: site.baseurl }}" class="post-link">{{ latest_post.title }} </a>
	</h3>
</div> -->