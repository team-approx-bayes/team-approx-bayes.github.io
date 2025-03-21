---
title: Variational Learning Induces Adaptive Label Smoothing 
date: 2025-03-15
categories:
  - blog
author: Emtiyaz Khan
---

Label Smoothing is a technique that replaces the original label with a smoothed version, which prevents overconfident predictions. Original label smoothing smooths the label with a uniform noise for all examples, while adaptive label smoothing customizes the noise for each example according to data characteristics. However, existing adaptive label smoothing methods require additional mechanisms to adjust the smoothing, e.g., adjust the smoothing after each epoch according to the model predictions. In [our recent work](https://arxiv.org/abs/2502.07273), we show that variational learning induces adaptive label smoothing without additional procedures. Empirical results demonstrate that this adaptive label smoothing is better than the constant noise from traditional label smoothing. 

Paper Link: [https://arxiv.org/abs/2502.07273](https://arxiv.org/abs/2502.07273)

## Why Variational Learning Has Adaptive Label Smoothing

Label Smoothing addes a noise $\epsilon$ to the original label $y$, which generates the smoothed label $y'=y+\epsilon$.

Variational learning minimizes the Evidence Lower Bound (ELBO) over a weight distribution $q$, while deep learning minimizes the empirical risk. When comparing their gradient descent updates over a model $f(x)$ in binary classification, we can see that variational learning indices noise:

$$
\epsilon = \sigma(f(x))- \mathbb{E}_q[\sigma(f(x))],
$$

where $\sigma(\cdot)$ is the Sigmoid function.

We plot the magnitude of the noise per example in the Moon dataset, to understand the noise better. When the prediction is uncertain, i.e., sigmoid value of the posterior $q$ mean is around 0.5, the noise is stronger. These points are around the boundary, where the model is uncertain.

**TODO: explain the plot and the corresponding meaning**

## Empirical Results
Emperiment results show that variational learning's adaptive label smoothing is better than the constant noise from original label smoothing. 


