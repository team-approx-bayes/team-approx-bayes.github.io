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

We plot the magnitude of the noise per example in the Moon dataset to understand the noise. When the prediction is uncertain, i.e., sigmoid value of the posterior $q$ mean is around 0.5, the noise is stronger. As shown in the figure, these points are around the boundary where the model is uncertain. The size and visibility of each point reflects the magnitude of noise on each points.

**Interactives:**\
To interact with the plot either **tap** or **drag over** your desired points of interest and **select** one of the color to highlight them in. **Deselect** by clicking any blank area of the plot.

<div style="width: 100%; max-width: 100%; overflow: hidden; height: 800px;">
  <div style="transform: scale(0.8); transform-origin: top left; width: calc(100% / 0.8); height: 900px; overflow: hidden;">
    <iframe src="/assets/visual/sigmoid_projection.html" width="100%" height="1000" style="border: none;"></iframe>
  </div>
</div>

For Neural Networks, since weight perturbation results in other kinds of noise in Jacobian and Hessian. We can derive the approximate noise: 

$$
\epsilon = \sigma'(f(x))\nabla f(x) \mathbf{\Sigma^{1/2} e},
$$

where $\mathbf{e}$ is a standard normal distribution. The noise is adjusted according to the example $x$ and the learned posterior covariance $\mathbf{\Sigma}$.


## Empirical Results
Emperiment results show that variational learning's adaptive label smoothing is better than the constant noise of the original label smoothing. We use a variational learning algorithm called IVON, and we analyze the label smoothing of it.

[//]: <> **TODO: Maybe show the MNIST plot here?**
[//]: <> Below we demonstrate how the assignment of Label-Noise changes over training iteration on MNIST. From top to bottom, the MNIST images are ordered from high to low Label-Noise for each segment. Sampling group of **High Label-Noise** and **Low Label-Noise**, as training goes on per iteration, it is visible that the update being done to Low Label-Noise groups is lessening compared to the rapid changing of High Label-Noise updates.

To visualize how adaptive label smoothing assign label-noise over training iteration, below plots samples of MNIST, high label-noise and low label-noise samples. Arranged from top to bottom, the MNIST images are arranged from high to low label-noise.

**Interactives:**\
**Slide the slider** or **hit play** to see how label-noise given to the MNIST samples changes over training.

<div style="width: 100%; max-width: 100%; overflow: hidden; height: 900px; display: flex; justify-content: center; align-items: flex-start;">
  <div style="transform: scale(1); transform-origin: top center; width: calc(100% / 0.75); height: 1000px; overflow: hidden;">
    <iframe src="/assets/visual/mnist_50_samples_100_mc.html" width="100%" height="1100" style="border: none;"></iframe>
  </div>
</div>
<br />

As training progresses, it's evident that samples in the High label-noise group are being updated more fequently than those in the Low label-noise group. This behavior demonstrates that IVON's adaptive label smoothing dynamically focuses the model's learning onto datapoints that are more uncertain, i.e. cases of labeling errors, distribution shift or calibration issues. This means that well understood samples remain stable, preserving generalization, preventing overconfidence. 

Below we demonstrate that IVON's smoothed label is similar to a existing adaptive label smoothing technique called [Online Label Smoothing (OLS)](https://arxiv.org/abs/2011.12562) without needing any additional effort to design or estimate the adaptive label noise. 

<div style="text-align: center; padding-bottom: 15px">
<img src="/assets/images/lsblog/olscompare.png" alt="Smoothed label comparison with OLS" style="width:100%;max-width:900px">
</div>

When data has labeling errors, experiment results show that IVON consistently outperforms traditional label smoothing, and comparable with [Sharpness Aware Minimization (SAM)](https://arxiv.org/abs/2010.01412).

To demonstrate how IVON performs against traditional Label Smoothing and SAM, below shows an experiment with data-dependent labeling errors on CIFAR-10. Each class are assigned a different level of label noise, with the correct label trained with certain probability, varrying among different classes. For each class, the correct label has a probability of $1 - (k + \beta i), i\in [1,K]$ where $k$ is the starting noise label and $\beta$ is the increasing factor. The remaining probability was then spread evenly across all the wrong labels of that class. Plotted result shows the best result selected from, LS with smoothing rate of {0, 0.1, 0.3, 0.5, 0.7, 0.9}, SAM with $\rho$ of {0, 0.05, 0.1, 0.15, 0.2, 0.5}. $\beta$ is kept at $0.05$ for this experiment.
<div style="text-align: center; padding-bottom: 15px">
<img src="/assets/images/lsblog/mislabel.png" alt="Comparison in labeling error scenario" style="width:100%;max-width:500px">
</div>

From the presented emperical result, we've successfully demonstrated the claim that adaptive label noise induced by variational learning is more effective than traditional label smoothing. IVON not only proves to be adaptive against varying label noise, but it also provides means of utilizing adaptive label smoothing without additional effort. We believe that variational learning algorithms, such as IVON, provide a flexible framework to further add noise to handle both the abnormalities and typicalities in the data.