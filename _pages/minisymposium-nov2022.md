---
layout: single
title: The ABI Team Seminar
permalink: /minisymposium/
author_profile: false
---
November 1st, 2022 at [RIKEN Center for AI Project, Tokyo](https://aip.riken.jp)

## Information
- This seminar includes a total of 7 talks from external visitors and
people from AIP
- Each talk is 40 minutes, with 10 minutes questions and discussion
  afterwards. All talks will be held in the open area at
  [RIKEN AIP](https://aip.riken.jp/access/)
- Participants can also join through Zoom. Register [here](https://c5dc59ed978213830355fc8978.doorkeeper.jp/events/145905) to see the link.
- For in-person attendance is only possible for AIP members
- [How to get to RIKEN-AIP](https://aip.riken.jp/access/) to see the link.

## Program
- 09:30 -- 09:55 Registration and setting up.
- **Session I** (Chair: [Gian Maria Marconi](https://gmmarconi.github.io))
  - 10:00 -- 10:50 [JinYeong Bak](https://nosyu.kr),
    *Natural Language Inference with Knowledge and Emotion-Cause Pair Extraction*, [abstract](#1)
  - 10:50 -- 11:40 [Thomas Möllenhoff](https://thomasmoellenhoff.net),
    *SAM as an Optimal Relaxation of Bayes*, [abstract](#2)
  - 11:40 -- 12:30 [Alexander Immer](https://aleximmer.github.io),
  *Scalable Bayesian Neural Network model selection*, [abstract](#3)
- 12:30 -- 14:00 Lunch break
- **Session II** (Chair: [Thomas Möllenhoff](https://thomasmoellenhoff.net))
  - 14:00 -- 14:50 [Mehmet Eren Kiral](https://ekiral.github.io),
    *The Lie Group Bayesian Learning Rule*, [abstract](#4)
  - 14:50 -- 15:40
    [Konstantinos Pitas](https://www.konstantinos-pitas.com), *Cold Posteriors through PAC-Bayes*, [abstract](#5)
- 15:40 -- 16:00 Coffee break
- **Session III** (Chair: [Jooyeon Kim](https://scholar.google.com/citations?user=ie5WNHcAAAAJ))
  - 16:00 -- 16:50
    [Carlo D'Eramo](https://www.ias.informatik.tu-darmstadt.de/Team/CarloDEramo),
    *Lightweight Reinforcement Learning for Autonomous Adaptive Agents*, [abstract](#6)
  - 16:50 -- 17:40
    [Georgia Chalvatzaki](https://www.ias.informatik.tu-darmstadt.de/Team/GeorgiaChalvatzaki),
        *Shaping Robotic Assistance through Structured Robot Learning*, [abstract](#7)
- 18:00 Concluding remarks

## Title and Abstracts
<a name="1"></a>
### [JinYeong Bak](https://nosyu.kr), Sung Kyun Kwan University
Title: Natural Language Inference with Knowledge and Emotion-Cause Pair Extraction

Abstract: In this talk, I will introduce two recent research projects on natural language inference (NLI) - incorporating knowledge for NLI and emotion recognition - incorporating meta information for identifying the cause of emotion in conversations. Finding counterevidence to statements is key to many tasks, including counter argument generation. We present a knowledge-enhanced NLI model that aims to handle causality- and example-based inference by incorporating knowledge graphs. Our NLI model outperforms baselines for NLI tasks, especially for instances that require the targeted inference. Second, the Emotion-Cause Pair Extraction (ECPE) task aims to pair all emotions and corresponding causes in documents. However, previous ECPE research is conducted based on news articles, which has different characteristics compared to dialogues. To address this issue, we propose a Pair-Relationship Guided Mixture-of-Experts (PRG-MoE) model, which considers dialogue features (e.g., speaker information). PRG-MoE automatically learns the relationship between utterances and advises a gating network to incorporate dialogue features in the evaluation, yielding substantial performance improvement.

<a name="2"></a>
### [Thomas Möllenhoff](https://thomasmoellenhoff.net), RIKEN AIP
Title: SAM as an Optimal Relaxation of Bayes

Abstract: Sharpness-aware minimization (SAM) and related adversarial deep-learning methods can drastically improve generalization, but their underlying mechanisms are not yet fully understood. Here, we establish SAM as a relaxation of the Bayes objective where the expected negative-loss is replaced by the optimal convex lower bound, obtained by using the so-called Fenchel biconjugate. The connection enables a new Adam-like extension of SAM to automatically obtain reasonable uncertainty estimates, while sometimes also improving its accuracy. By connecting adversarial and Bayesian methods, our work opens a new path to robustness.

<a name="3"></a>
###  [Alexander Immer](https://aleximmer.github.io), ETH Center for Learning Systems
Title: Scalable Bayesian Neural Network model selection

Abstract: Alexander will present a method for scalable Bayesian neural network model selection, which relies on estimation and optimization of the marginal likelihood. Marginal-likelihood based model selection, even though promising, is rarely used in deep learning due to estimation difficulties. Instead, most approaches rely on validation data, which may not be readily available. The proposed method allows to optimize hyperparameters, such as regularization strength and architecture, but also invariances, based on training data alone. Notably, many hyperparameters can be optimized online during training. The marginal likelihood estimate is based on Laplace's method and Gauss-Newton approximations to the Hessian, and it can even outperform cross-validation, especially when many hyperparameters need to be optimized. The talk will finish with a discussion of the algorithm and potential reasons for its effectiveness.

<a name="4"></a>
### [Mehmet Eren Kiral](https://ekiral.github.io), RIKEN AIP
Title:  The Lie Group Bayesian Learning Rule

Abstract: I will talk about our recent work with Thomas Möllenhoff and Emtiyaz Khan where we find update rules for the Bayesian Learning Problem using a Lie group structure on the information manifold. The set of candidate distributions (on the model parameters) is parametrized by a Lie group and then the updates of distributions are given by updating the group elements. The Lie group's exponential map and homogeneity properties are used to write down the rule.


<a name="5"></a>
###  [Konstantinos Pitas](https://www.konstantinos-pitas.com), INRIA Grenoble
Title: Cold Posteriors through PAC-Bayes

Abstract: We investigate the cold posterior effect through the lens of PAC-Bayes generalization bounds. We argue that in the non-asymptotic setting, when the number of training samples is (relatively) small, discussions of the cold posterior effect should take into account that approximate Bayesian inference does not readily provide guarantees of performance on out-of-sample data. Instead, out-of-sample error is better described through a generalization bound. In this context, we explore the connections of the ELBO objective from variational inference and the PAC-Bayes objectives. We note that, while the ELBO and PAC-Bayes objectives are similar, the latter objectives naturally contain a temperature parameter λ which is not restricted to be λ = 1. For both regression and classification tasks, in the case of isotropic Laplace approximations to the posterior, we show how this PAC-Bayesian interpretation of the temperature parameter captures important aspects of the cold posterior effect.

<a name="6"></a>
### [Carlo D'Eramo](https://www.ias.informatik.tu-darmstadt.de/Team/CarloDEramo), TU Darmstadt
Title: Lightweight Reinforcement Learning for Autonomous Adaptive Agents

Abstract: Future intelligent agents need to autonomously act in rich dynamic environments, e.g., industrial plants, finance, healthcare, replacing or collaborating with humans in dangerous and tedious tasks. Reinforcement Learning (RL) is a well-established field of study to model how agents autonomously learn to act, which burst since the recent coupling with deep learning methods (deep RL), achieving groundbreaking results in previously unsolvable problems. Juxtaposed with the extraordinary results of deep RL is the realisation that its methods cannot be used out-of-the-box, especially for real-world problems, due to strong inefficiency issues and need of human supervision.
In this talk, I will describe my research revolving around the problem of how agents can efficiently acquire expert skills that account for the complexity of the real world. My research aims to answer this question by introducing lightweight (deep) RL methods for obtaining autonomous and adaptive agents efficiently. I will explain my recent contributions, particularly focusing on the motivations behind each work and on the significance of the achieved results. Through the description of my works, this talk has the additional goal of providing a synthetic but effective overview of the current limits of deep RL, and suggesting possible future research directions worth exploring.


<a name="7"></a>
### [Georgia Chalvatzaki](https://www.ias.informatik.tu-darmstadt.de/Team/GeorgiaChalvatzaki), TU Darmstadt
Title: Shaping Robotic Assistance through Structured Robot Learning

Abstract: Future intelligent robotic assistants are expected to perform various tasks in unstructured and human-inhabited environments. These robots should support humans in everyday activities as personal assistants or collaborate with them in work environments like hospitals and warehouses. In this talk, I will briefly describe my research works for robotic assistants to help and support humans in need, developing specific human-robot interaction behaviors combining classical robotics and machine learning approaches. I will then explain how mobile manipulation robots are currently the most promising solution among embodied AI systems, thanks to their body structure and sensorial equipment for learning to execute a series of assistive tasks. On top of this, I will point out some key challenges that hinder autonomous mobile manipulation for intelligent assistance and discuss how structured robot learning can pave the way toward generalizable robot behaviors. Structured robot learning refers to all learning methods at the intersection of classical robotics and machine learning that aim to leverage structure in data and algorithms to scale robot behaviors to complex tasks. Finally, this talk will give insights into how my team and I leverage structured representations, priors, and task descriptions together with learning and planning in some challenging (mobile) manipulation tasks in our path for creating general-purpose intelligent robotic assistants.

