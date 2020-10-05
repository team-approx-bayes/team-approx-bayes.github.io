---
layout: single
title: Blog
permalink: /blog/
author_profile: false
---

{% assign posts = site.posts %}
{% assign entries_layout = page.entries_layout | default: 'list' %}
{% for post in posts %}
{% if post.categories contains 'blog' %}
<div class="post">
<h3>
      <a href="{{ post.url | prepend: site.baseurl }}" class="post-link">
        {{ post.title }}
		</a>
		</h3>
		<p class="post-summary">
        <span class="post-meta">{{ post.date | date: '%B %d, %Y'  }}.&nbsp;&nbsp;</span>
{{ post.content | strip_html | truncatewords:35}} <a href="{{ post.url }}">Continue</a>
</p>
</div>

  {% endif %}
{% endfor %}





