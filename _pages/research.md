---
layout: single
title: Outline
permalink: /research/
author_profile: false
custom_css: research
---
[**[Research]**](#research)   [**[Blog]**](#blog)  [**[Talk]**](#talk)  [**[Code]**](#code)

# Research
Humans, animals, and other living beings have a natural ability to autonomously learn throughout their lives and quickly adapt to their surroundings, but computers lack such abilities.
Our goal is to bridge such gaps between the learning of living-beings and computers.
We are machine learning researchers with an expertise in areas such as approximate inference, Bayesian statistics, continuous optimization, information geometry etc.
We work on a variety of learning problems, especially those involving supervised, continual, active, federated, online, and reinforcement learning.

Currently, we are developing algorithms which enable computers to autonomously learn to perceive, act, and reason throughout their lives.
Our research often brings together ideas from a variety of theoretical and applied fields, such as, mathematical optimization,
Bayesian statistics, information geometry, signal processing, and control systems.

For more information, see our current [publications](../publications/) and the following pages:

<ul class="w3-ul">
  <li> <a href="https://bayesduality.github.io" target="_blank">The Bayes-Duality Project</a> (funded by CREST)</li>
  <li> Summary of research for the year [<a href="https://emtiyaz.github.io/papers/symposium_2024.pdf" target="_blank">2024</a>] [<a href="https://emtiyaz.github.io/papers/symposium_2023.pdf" target="_blank">2023</a>] [<a href="https://emtiyaz.github.io/papers/symposium_2022.pdf" target="_blank">2022</a>] [<a href="https://emtiyaz.github.io/papers/symposium_2021.pdf" target="_blank">2021</a>] [<a href="https://emtiyaz.github.io/papers/symposium_2019.pdf" target="_blank">2019</a>] [<a href="https://emtiyaz.github.io/papers/symposium_2018.pdf" target="_blank">2018</a>] [<a href="https://emtiyaz.github.io/papers/symposium_2017.pdf" target="_blank">2017</a>] </li>
</ul>

We are also thankful to receive the following external funding (funding amount is approximate),
<ul class="w3-ul">
  <li> (2023-2026, USD 32,000) KAKENHI Grant-in-Aid for Early-Career Scientists, [<a href="https://kaken.nii.ac.jp/en/grant/KAKENHI-PROJECT-23K13024/" target="_blank">23K13024</a>] </li>
  <li> (2021-2026, USD 2.23 Million) JST-CREST and French-ANR's grant, <a href="https://bayesduality.github.io" target="_blank">The Bayes-Duality Project</a></li>
  <li> (2020-2023, USD 167,000) KAKENHI Grant-in-Aid for scientific Research (B), Life-Long Deep Learning using Bayesian Principles </li>
  <li> (2019-2022, USD 237,000) External funding through companies for several Bayes related projects</li> 
</ul>	

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

# Videos

<div class="w3-container">
<ul class="w3-ul">
     <li>
	    [June 27th, 2025]
        <span class="title">The 3rd Bayes-Duality Workshop 2025: Day 3</span>
        [<a href="https://www.youtube.com/watch?v=wwR8O38jGH4" target="_blank">Video</a>]
     </li>
     <li>
	    [June 26th, 2025]
        <span class="title">The 3rd Bayes-Duality Workshop 2025: Day 2</span>
        [<a href="https://www.youtube.com/watch?v=WMZImIQ14Lk" target="_blank">Video</a>]
     </li>
     <li>
	    [June 25th, 2025]
        <span class="title">The 3rd Bayes-Duality Workshop 2025: Day 1</span>
        [<a href="https://www.youtube.com/watch?v=Ly5fPJQY5zM" target="_blank">Video</a>]
     </li>
     <li>
        [July 30th, 2024] <a href="https://emtiyaz.github.io/" target="_blank">Emtiyaz Khan</a>:
        <span class="title">Keynote at the <a href="https://lifelong-ml.cc/" target="_blank">3rd Conference on Lifelong Learning Agents (CoLLAs) 2024</a></span>,
        [<a href="https://emtiyaz.github.io/papers/July30_2024_CoLLAs.pdf" target="_blank">Slides</a>]
	    [<a href="https://youtu.be/_49ydwCrhVk?feature=shared" target="_blank">Video</a>]
     </li>
</ul>
</div>

# Code
Here we list research code that has been open-sourced to accompany recent publications. Our team's github homepage: [https://github.com/team-approx-bayes](https://github.com/team-approx-bayes).

<div class="w3-container">
<ul class="w3-ul">
    <li>
      <span class="conf">(<a href="https://sites.google.com/view/neurips2024-ftw/home" target="_blank">Fine-Tuning in Modern ML (FITML)</a>)</span>
      <span class="title">Variational Low-Rank Adaptation Using IVON</span>,
      [<a href="https://arxiv.org/abs/2411.04421" target="_blank">arXiv</a>]
	    [<a href="https://github.com/team-approx-bayes/ivon-lora" target="_blank">Code</a>]
    </li>
    <li>
		   <span class="conf">(<a href="https://icml.cc/" target="_blank">ICML 2024</a>)</span>
        <span class="title">Variational Learning is Effective for
		Large Deep Networks</span>,
        [<a href="https://arxiv.org/abs/2402.17641" target="_blank">arXiv</a>]
	    [<a href="https://github.com/team-approx-bayes/ivon" target="_blank">Code</a>]
    </li>

     <li>
		   <span class="conf">(<a href="https://iclr.cc/" target="_blank">ICLR 2024</a>)</span>
        <span class="title">Model Merging by Uncertainty-Based
		Gradient Matching</span>,
        [<a href="https://arxiv.org/abs/2310.12808" target="_blank">arXiv</a>]
	    [<a href="https://github.com/UKPLab/iclr2024-model-merging" target="_blank">Code</a>]
     </li>
     <li>
 	    <span class="conf">(<a href="https://iclr.cc/" target="_blank">ICLR 2024</a>)</span>
 <span class="title">Conformal Prediction via Regression-as-Classification</span>,
        [<a href="https://etash.me/papers/Bayesian_Conformal_Prediction_through_Memory_Adaptation.pdf" target="_blank">preprint</a>]
	    [<a href="https://github.com/EtashGuha/R2CCP" target="_blank">Code</a>]
     </li>

   <li>
   		  <span class="conf">(<a
		  href="https://neurips.cc/">NeurIPS 2023</a>)</span>
         <span class="title">The Memory Perturbation Equation:
   		  Understanding Models' Sensitivity to Data</span>
         [<a href="https://arxiv.org/pdf/2310.19273" target="_blank">arXiv</a>]	    [<a href="https://github.com/team-approx-bayes/memory-perturbation" target="_blank">Code</a>]
		 </li>
  
  <li>
   		  <span class="conf">(<a
		  href="https://jmlr.org/tmlr/">TMLR 2023</a>)</span>
         <span class="title">Improving Continual Learning by Accurate Gradient Reconstructions of the Past</span>
         [<a href="https://openreview.net/pdf?id=b1fpfCjja1" target="_blank">Published Version</a>] [<a href="https://github.com/team-approx-bayes/ewc-fr-replay" target="_blank">Code</a>]
		 </li>

   <li>
   		  <span class="conf">(<a
		  href="http://aistats.org">AISTATS 2023</a>)</span>
         <span class="title">The Lie-Group Bayesian Learning Rule</span>
         [<a href="https://arxiv.org/abs/2303.04397" target="_blank">arXiv</a>] [<a href="https://github.com/team-approx-bayes/liegroups" target="_blank">Code</a>]
		 </li>

   <li>
   		  <span class="conf">(<a
   		  href="http://iclr.cc">ICLR 2023</a>)</span>
         <span class="title">SAM as an Optimal Relaxation of Bayes</span>
         [<a href="https://arxiv.org/abs/2210.01620" target="_blank">arXiv</a>] [<a href="https://github.com/team-approx-bayes/bayesian-sam" target="_blank">Code</a>]
	</li>

   <li>
   		  <span class="conf">(<a href="https://papers.nips.cc/paper/2021/">NeurIPS 2021</a>)</span>
         <span class="title">Knowledge-Adaptation Priors.</span>
         [<a href="http://arxiv.org/abs/2106.08769" target="_blank">arXiv</a>] [<a href="papers/July23_2021_CL_workshop.pdf" target="_blank">Slides</a>] [<a href="https://t.co/v68OrIE0Xz?amp=1" target="_blank">Tweet</a>] [<a href="https://t.co/XBRwRh3Lde?amp=1" target="_blank">SlidesLive Video</a>]  [<a href="https://github.com/team-approx-bayes/kpriors" target="_blank">Code</a>]
	</li>

  <li>
         <span class="conf">(<a href="https://papers.nips.cc/paper/2021/">NeurIPS 2021</a>)</span>
         <span class="title">Dual Parameterization of Sparse Variational Gaussian Processes.</span>
         [<a href="https://arxiv.org/abs/2111.03412" target="_blank">arXiv</a>]
         [<a href="https://github.com/AaltoML/t-SVGP" target="_blank&quot;">Code</a>]    
      </li>


  <li>
       <span class="conf">(<a href="http://proceedings.mlr.press/v130/" target="_blank">AISTATS 2021</a>)</span>
       <span class="title"> Improving predictions of Bayesian neural networks via local linearization.</span>
       [<a href="https://proceedings.mlr.press/v130/immer21a.html" target="_blank">Published version</a>]
       [<a href="https://arxiv.org/pdf/2008.08400" target="_blank">arXiv</a>]
       [<a href="https://github.com/AlexImmer/BNN-predictions" target="_blank&quot;">Code</a>]
  </li>

  <li>
     <span class="conf">(<a href="http://proceedings.mlr.press/v139/" target="_blank">ICML 2021</a>)</span>
     <span class="title">Scalable Marginal Likelihood Estimation for Model Selection in Deep Learning.</span>
       [<a href="http://proceedings.mlr.press/v139/immer21a.html" target="_blank">Published version</a>]
     [<a href="https://arxiv.org/abs/2104.04975" target="_blank">arXiv</a>]
     [<a href="https://github.com/AlexImmer/marglik" target="_blank&quot;">Code</a>]
   </li>

  <li>  
         <span class="conf">(<a href="https://auai.org/uai2021/accepted_papers" target="_blank">UAI 2021</a>)</span>  
         <span class="title">Subset-of-Data Variational Inference for Deep Gaussian-Process Regression.</span>
          [<a href="https://arxiv.org/abs/2107.08265" target="_blank">arXiv</a>]
          [<a href="https://github.com/brain-iith/SOD_DGP" target="_blank&quot;">Code</a>]  
   </li>

    <li>
          <span class="conf">(<a href="https://papers.nips.cc/paper/2020/" target="_blank">NeurIPS 2020</a>)</span>
         <span class="title">Continual Deep Learning by Functional Regularisation of Memorable Past.</span>
         [<a href="https://papers.nips.cc/paper/2020/hash/2f3bbb9730639e9ea48f309d9a79ff01-Abstract.html" target="_blank">Published version</a>]
         [<a href="https://arxiv.org/abs/2004.14070" target="_blank">ArXiv</a>]
         [<a href="https://github.com/team-approx-bayes/fromp" target="_blank">Code</a>]
         [<a href="FROMP_NeurIPS2020_poster.pdf" target="_blank">Poster</a>]
    </li>

      <li>
          <span class="conf">(<a href="https://icml.cc/Conferences/2020/AcceptedPapersInitial" target="_blank">ICML 2020</a>)</span>
         <span class="title">Handling the Positive-Definite Constraint in the Bayesian Learning Rule.</span>
   [<a href="http://proceedings.mlr.press/v119/lin20d.html" target="_blank">Published version</a>] 
         [<a href="https://arxiv.org/abs/2002.10060" target="_blank">arXiv</a>]
         [<a href="https://github.com/yorkerlin/iBayesLRule" target="_blank&quot;">Code</a>]
      </li>

      <li>
         <span class="conf">(<a href="https://icml.cc/Conferences/2020/AcceptedPapersInitial" target="_blank">ICML 2020</a>)</span>
         <span class="title">Training Binary Neural Networks using the Bayesian Learning Rule.</span>
	 [<a href="http://proceedings.mlr.press/v119/meng20a.html" target="_blank">Published version</a>] 
         [<a href="https://arxiv.org/abs/2002.10778" target="_blank">arXiv</a>] [<a href="https://github.com/team-approx-bayes/BayesBiNN" target="_blank&quot;">Code</a>]
      </li>

      <li>
          <span class="conf">(<a href="https://icml.cc/Conferences/2020/AcceptedPapersInitial" target="_blank">ICML 2020</a>)</span>
         <span class="title">VILD: Variational Imitation Learning with Diverse-quality Demonstrations.</span>
   [<a href="http://proceedings.mlr.press/v119/tangkaratt20a.html" target="_blank">Published version</a>]
         [<a href="https://arxiv.org/abs/1909.06769" target="_blank">arXiv</a>]
         [<a href="https://github.com/voot-t/vild_code" target="_blank&quot;">Code</a>]
      </li>

            <li>
      <span class="conf">(<a href="https://nips.cc/Conferences/2019" target="_blank">NeurIPS 2019</a>)</span> 
      <span class="title">Practical Deep Learning with Bayesian Principles.</span>
      [<a href="https://proceedings.neurips.cc/paper/2019/hash/b53477c2821c1bf0da5d40e57b870d35-Abstract.html" target="_blank">Published version</a>]
      [<a href="https://arxiv.org/abs/1906.02506" target="_blank">arXiv</a>] [<a href="https://github.com/team-approx-bayes/dl-with-bayes" target="_blank&quot;">Code</a>]
      </li>

            <li>
       <span class="conf">(<a href="https://nips.cc/Conferences/2019" target="_blank">NeurIPS 2019</a>)</span>
      <span class="title">Approximate Inference Turns Deep Networks into Gaussian Processes.</span>
      [<a href="https://proceedings.neurips.cc/paper/2019/hash/b3bbccd6c008e727785cb81b1aa08ac5-Abstract.html" target="_blank">Published version</a>]
      [<a href="https://arxiv.org/abs/1906.01930" target="_blank">arXiv</a>] [<a href="https://github.com/team-approx-bayes/dnn2gp" target="_blank&quot;">Code</a>]
      </li>


            <li>
       <span class="conf">(<a href="https://icml.cc/" target="_blank">ICML, 2019</a>)</span> 
      <span class="title">Fast and Simple Natural-Gradient Variational Inference with Mixture of Exponential-family Approximations.</span><br>
      [<a href="https://arxiv.org/abs/1906.02914" target="_blank">arXiv</a>] [<a href="http://proceedings.mlr.press/v97/lin19b.html" target="_blank">Published version</a>][<a href="https://github.com/yorkerlin/VB-MixEF" target="_blank&quot;">Code</a>]<br>
      </li>

            <li>
      <span class="conf">(<a href="https://icml.cc/" target="_blank">ICML, 2019</a>)</span>
      <span class="title">Scalable Training of Inference Networks for Gaussian-Process Models.</span>
      [<a href="https://arxiv.org/abs/1905.10969" target="_blank">arXiv</a>] [<a href="http://proceedings.mlr.press/v97/shi19a.html" target="_blank"> Published version</a>][<a href="https://github.com/thjashin/gp-infer-net" target="_blank&quot;">Code</a>]
      </li>

            <li>
       <span class="conf">(<a href="https://nips.cc/Conferences/2018/Schedule?showEvent=11605" target="_blank">NeurIPS 2018</a>)</span>
      <span class="title">SLANG: Fast Structured Covariance Approximations for Bayesian Deep Learning with Natural Gradient.</span><br>
 	 [<a href="https://proceedings.neurips.cc/paper/2018/hash/d3157f2f0212a80a5d042c127522a2d5-Abstract.html" target="_blank"> Published version</a>]
         [<a href="http://arxiv.org/abs/1811.04504" target="_blank">arXiv</a>]
         [<a href="https://github.com/aaronpmishkin/SLANG/blob/master/poster/SLANG_NIPS_2018_Poster.pdf" target="_blank">Poster</a>]
         [<a href="https://www.youtube.com/watch?v=ekaB_weR5Bw&amp;feature=youtu.be" target="_blank">3-min Video</a>]
         [<a href="https://github.com/aaronpmishkin/SLANG" target="_blank">Code</a>]
      </li>

            <li>
       <span class="conf">(<a href="https://icml.cc/" target="_blank">ICML 2018</a>)</span> 
      <span class="title">Fast and Scalable Bayesian Deep Learning by Weight-Perturbation in Adam.</span>
         [<a href="http://proceedings.mlr.press/v80/khan18a.html" target="_blank"> Published version</a>]
         [<a href="https://arxiv.org/abs/1806.04854" target="_blank">arXiv</a>]
         [<a href="https://github.com/emtiyaz/vadam/" target="_blank">Code</a>]
         [<a href="papers/icml2018_slides.pdf" target="_blank">Slides</a>]
      </li>

            <li>  
      <span class="conf">(<a href="https://iclr.cc/" target="_blank">ICLR 2018</a>)</span>
      <span class="title">Variational Message Passing with Structured Inference Networks.</span>
         [<a href="https://openreview.net/forum?id=HyH9lbZAW" target="_blank">Paper</a>]
         [<a href="http://arxiv.org/abs/1803.05589" target="_blank">arXiv Version</a>]
         [<a href="https://github.com/emtiyaz/vmp-for-svae/" target="_blank">Code</a>]
      </li>

           <li> 
       <span class="conf">(<a href="http://www.aistats.org/" target="_blank">AIstats 2018</a>)</span>
      <span class="title">Bayesian Nonparametric Poisson-Process Allocation for Time-Sequence Modeling.</span>
	[<a href="http://proceedings.mlr.press/v84/ding18a.html" target="_blank">Published version</a>]
	[<a href="https://github.com/Dinghy/BaNPPA" target="_blank">Code</a>]
      </li>

   <li id="#aistats2017">
    <span class="conf">(<a href="http://www.aistats.org/" target="_blank">AIstats 2017</a>)</span>
	<span class="title">Conjugate-Computation Variational Inference : Converting Variational Inference in Non-Conjugate Models to Inferences in Conjugate Models.</span>
	[<a href="http://proceedings.mlr.press/v54/khan17a.html" target="_blank"> Published version </a>]
	[<a href="https://arxiv.org/abs/1703.04265" target="_blank">arXiv </a>]
	[<a href="https://github.com/emtiyaz/cvi/" target="_blank">Code for Logistic Reg + GPs</a>]
	[<a href="https://github.com/emtiyaz/cvi/" target="_blank">Code for Correlated Topic Model</a>]
    </li>

    <li>
    <span class="conf">(<a href="https://www.ieee-security.org/TC/SP2017/" target="_blank">38th IEEE Symposium on Security and Privacy 2017(S&amp;P))</a></span>
	<span class="title">SmarPer: Context-Aware and Automatic Runtime-Permissions for Mobile Devices.</span>
[<a href="https://doi.org/10.1109/SP.2017.25" target="_blank">Published paper</a>]
[<a href="https://github.com/lca1/smarper" target="_blank">Code</a>]
[<a href="https://spism.epfl.ch/smarper/" target="_blank">SmarPer Homepage</a>]
		</li>

    <li id="#bs2017">
    <span class="conf">(<a href="http://www.buildingsimulation2017.org/" target="_blank">Building Simulation 2017</a>)</span>
	<span class="title">Gaussian-Process-Based Emulators for Building Performance Simulation.</span><br>
	[<a href="papers/Building_Simulation.pdf" target="_blank">Paper</a>]
	[<a href="https://zenodo.org/record/291858#.WME-XBKGNo4" target="_blank">Building Simulation Data</a>]
	[<a href="https://github.com/paragrastogi/GPregressionInBS" target="_blank">Code</a>]
		</li>
</ul>
</div>
<div style="pointer-events: none !important; display: none !important; position: absolute; top: 0px !important; left: 0px !important; z-index: 2147483647 !important; box-sizing: content-box !important;">
