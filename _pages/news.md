---
layout: single
title: News
permalink: /news/
author_profile: false
---

{% for post in site.posts %}
{% if post.categories contains 'pinned-news' %}
<div class="news">
<i class="fa fa-thumbtack"></i>  <b> {{ post.title }} </b> <br>
{{ post.content }}
<hr>
</div>
{% endif %}
{% endfor %}

{% for post in site.posts %}
{% if post.categories contains 'news' %}
<div class="news">
<i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> <br>
{{ post.content }}
<hr>
</div>
{% endif %}
{% endfor %}

