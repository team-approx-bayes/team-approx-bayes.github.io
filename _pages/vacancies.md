---
layout: single
title: Vacanceis
permalink: /vacancies/
author_profile: false
---

{% for post in site.posts %}
{% if post.categories contains 'vacancies' %}
<div class="vacancies">
 <b class="news-title"> <i class="fa fa-thumbtack"></i>  <b> {{ post.title }} </b> </b> <br>
{{ post.content }}
<hr>
</div>
{% endif %}
{% endfor %}

{% include feature_row type="left" %}
