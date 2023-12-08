---
layout: single
title: Vacancies
permalink: /vacancies/
author_profile: false
---
<h2>Open Positions</h2>
{% for post in site.posts %}
{% if post.categories contains 'vacancies' %}
<div class="vacancies">
 <b class="news-title"> <i class="fa fa-thumbtack"></i>  <b> {{ post.title }} </b> </b> <br>
  <details>
    <summary>view content & link</summary>
    {{ post.content }}
  </details>
<hr>
</div>
{% endif %}
{% endfor %}
<h2>
RIKEN's Programs for Junior Scientists
<img src="/assets/images/riken_junior_scientists.jpg" alt="Logo" style="vertical-align:middle;" width="150" height="150">
</h2>
{% for post in site.posts %}
{% if post.categories contains 'vacancies-js' %}
<div class="vacancies-js">
 <b class="news-title"> <i class="fa fa-thumbtack"></i>  <b> {{ post.title }} </b> </b> <br>
  <details>
    <summary>view content & link</summary>
    {{ post.content }}
  </details>
<hr>
</div>
{% endif %}
{% endfor %}

{% include feature_row type="left" %}
