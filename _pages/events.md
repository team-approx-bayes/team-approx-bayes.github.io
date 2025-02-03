---
layout: single
title: Events
permalink: /events/
author_profile: false
---

Events for ABI Team:
<ul class="w3-ul">
  <li> <strong><em>Reading Group</em></strong> : Every two weeks, a different group member takes the lead, presenting a chosen paper for discussion. (moderator: Thomas, duration: 60minutes) </li>
  <li> <em><strong>Tech Coffee</strong></em> : Every two weeks, a different full-time member takes the lead. The sessions focus on technical or mathematical aspects of our members' ongoing research projects. (moderator: Keigo, duration: 90minutes)</li>
  <li> <em><strong>Seminar</strong></em> : We frequently invite external speakers to give talks or tutorials. (moderator: Thomas) </li>
  <li> <em><strong>Meta Meals</strong></em> : Every two weeks, we hold guided discussions over lunch on research and more general topics. (moderator: Hugo, duration: 60minutes)</li> 
</ul>	

<strong>Other lab events</strong>: Writeups: Yohan, Bayes Duality Seminar: Hugo, Intern Writeups: Anita. \
<strong>Other lab operations</strong>: Hiring: Emti, Intern Hiring: Emti, Thomas, Wiki: Christopher, Webpage Maintainence: Keigo, Sin-Han, Purchase: Hugo, Emti, Thomas, Servers: Christopher, Hugo, Social Activity: Hugo. 

<h2>Upcoming</h2>

<section class="page__content cf">

{% capture curDate %}{{ site.time | date: '%F' }}{% endcapture %}
{% for post in site.posts %}
  {% capture postStartDate %}{{ post.date | date: '%F' }}{% endcapture %}
  {% if post.categories contains "seminar" and postStartDate >= curDate %}
    <div class="news">
    <b class="news-title"> <i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b>
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
    <b class="news-title"> <i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> </b> <br>
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
      <b class="news-title"> <i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> </b> <br>
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