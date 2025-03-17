---
title: Variational Learning Induces Adaptive Lable Smoothing 
date: 2025-03-15
categories:
  - blog
author: Emtiyaz Khan
---

Label Smoothing is a technique that replaces the original label with a smoothed version, which prevents overconfident predictions. Original label smoothing smooths the label with a uniform noise for all examples, while adaptive label smoothing customizes the noise for each example according to data characteristics. However, existing adaptive label smoothing methods require additional mechanisms to adjust the smoothing, e.g., adjust the smoothing after each epoch according to the model predictions. In [our recent work](https://arxiv.org/abs/2502.07273), we show that variational learning induces adaptive label smoothing without additional procedures. Empirical results demonstrate that this adaptive label smoothing is better than the constant noise from traditional label smoothing. 

Paper Link: [https://arxiv.org/abs/2502.07273](https://arxiv.org/abs/2502.07273)

## Why Variational Learning Has Adaptive Label Smoothing

## Empirical Results
Emperiment results show that variational learning's adaptive label smoothing is better than the constant noise from original label smoothing. 


