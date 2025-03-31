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

We plot the magnitude of the noise per example in the Moon dataset to understand the noise. When the prediction is uncertain, i.e., sigmoid value of the posterior $q$ mean is around 0.5, the noise is stronger. As shown in the figure, these points are around the boundary where the model is uncertain.

**TODO: explain the plot and the corresponding meaning**


For Neural Networks, since weight perturbation results in other kinds of noise in Jacobian and Hessian. We can derive the approximate noise: 

$$
\epsilon = \sigma'(f(x))\nabla f(x) \mathbf{\Sigma^{1/2} e},
$$

where $\mathbf{e}$ is a standard normal distribution. The noise is adjusted according to the example $x$ and the learned posterior covariance $\mathbf{\Sigma}$.


## Empirical Results
Emperiment results show that variational learning's adaptive label smoothing is better than the constant noise of the original label smoothing. We use a variational learning algorithm called IVON, and we analyze the label smoothing of it.

We show that IVON's smoothed label is similar to a previous adaptive label smoothing called [Online Label Smoothing (OLS)](https://arxiv.org/abs/2011.12562). 

<div style="text-align: center; padding-bottom: 15px">
<img src="/assets/images/lsblog/olscompare.png" alt="Smoothed label comparison with OLS" style="width:100%;max-width:900px">
</div>

When the data has labeling errors, experiment results show that IVON consistently outperforms traditional label smoothing, and comparable with [Sharpness Aware Minimization (SAM)](https://arxiv.org/abs/2010.01412).


<div style="text-align: center; padding-bottom: 15px">
<img src="/assets/images/lsblog/mislabel.png" alt="Comparison in labeling error scenario" style="width:100%;max-width:500px">
</div>
