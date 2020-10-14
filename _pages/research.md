---
layout: single
title: Research Areas
permalink: /research/
author_profile: false
---

Our research group is working on a range of topics in machine learning, such as approximate inference, deep learning, reinforcement learning, active learning and online learning.
The goal is to understand the fundamental principles which enable machines to learn from data, and use them to develop algorithms which bridge the gap between the learning of machines
and living-beings.

The current focus is on developing new algorithms which enable machines to autonomously learn to percept, act, and reason throughout their lives.
Our research often brings together ideas from a variety of theoretical and applied fields, such as, mathematical optimization,
Bayesian statistics, information geometry, signal processing, and control systems.

For more information, see our current [publications](../publications/).

# Blog
This blog provides a medium for our researchers to present their recent research findings, insights and updates. The posts in the blog
are written with a general audience in mind and provide an accessible introduction to our research. 

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





