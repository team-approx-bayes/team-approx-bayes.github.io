---
layout: single
title: Research
permalink: /research/
author_profile: false
---

Humans, animals, and other living beings have a natural ability to autonomously learn throughout their lives and quickly adapt to their surroundings, but computers lack such abilities.
Our goal is to bridge such gaps between the learning of living-beings and computers.
We are machine learning researchers with an expertise in areas such as approximate inference, Bayesian statistics, continuous optimization, information geometry etc.
We work on a variety of learning problems, especially those involving supervised, continual, active, federated, online, and reinforcement learning.

Currently, we are developing algorithms which enable computers to autonomously learn to perceive, act, and reason throughout their lives.
Our research often brings together ideas from a variety of theoretical and applied fields, such as, mathematical optimization,
Bayesian statistics, information geometry, signal processing, and control systems.

For more information, see our current [publications](../publications/).

# Blog
This blog provides a medium for our researchers to present their recent research findings, insights and updates. The posts in the blog
are written with a general audience in mind and aim to provide an accessible introduction to our research.

{% assign posts = site.posts %}
{% assign entries_layout = page.entries_layout | default: 'list' %}
{% for post in posts %}
  {% if post.categories contains 'blog' %}
  {% if post.external_url %}
<div class="post">
<h3>
      <a href="{{post.external_url}}" class="post-link">
        {{ post.title }}
		</a>
		</h3>
		<p class="post-summary">
        <span class="post-meta">{{ post.date | date: '%B %d, %Y'  }}.&nbsp;&nbsp;</span>
{{ post.content | strip_html | truncatewords:35}} <a href="{{ post.external_url }}">Continue</a>
</p>
</div>
  {% else %}
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
  {% endif %}
{% endfor %}

# Code
Here we list research code that has been open-sourced to accompany recent publications.
