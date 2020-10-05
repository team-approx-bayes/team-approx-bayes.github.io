---
layout: single
title: Reading Group and Internal Talks
permalink: /seminar/
author_profile: false
---

<section class="page__content cf">

{% for post in site.posts %}
  {% if post.categories contains 'seminar' %}
    <div class="news">
       <i class="fa {{post.logo}}"></i> <b> {{ post.date | date: '%B %d, %Y' }} </b> <br>
      {{ post.content }}
      <hr>
    </div>
  {% endif %}
{% endfor %}

</section>

* [25/09/2020] **Seminar** - [François-Xavier Briol](https://fxbriol.github.io/) (UCL): Stein's Method for Computational Statistics and Machine Learning

* [11/09/2020] **Reading group** - Survey on federated learning [ [Slides](/assets/rgroups/federated_learning.pdf) ]

* [04/09/2020] **Reading Group** - Survey on Transfer Learning [ [Slides](/assets/rgroups/transfer_learning.pdf) ]

* [28/08/2020] **Discussion** - Lab members projects overview <!--[ [Slides](/assets/rgroups/lab_overview.pdf) ]-->

* [21/08/2020] **Discussion** - Pierre's grant presentation rehearsal

* [14/08/2020] **Reading Group** - Gradient descent for wide two-layer neural networks [ [Blog post](https://francisbach.com/gradient-descent-for-wide-two-layer-neural-networks-implicit-bias/) ]

* [07/08/2020] **Reading Group** - Generalized Variational Inference: Three arguments for deriving new posteriors [ [Paper](https://arxiv.org/pdf/1904.02063.pdf) ]

* [31/07/2020] **Reading Group** - On the measure of intelligence  [ [Paper](https://arxiv.org/abs/1911.01547) ]

* [03/07/2020] **Reading Group** - Involutive MCMC: one way to derive them all [ [Paper](https://arxiv.org/abs/2006.16653) ]


