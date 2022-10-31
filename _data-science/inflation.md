---
layout: page
title: Visualizing Inflation in the US.
description: 
img: /assets/img/genre.gif
importance: 2
redirect_to: https://shruti-misra.github.io/inflation_viz/
category: visualization
---

**Concepts learned:** Multi-view compositions, zooming, scaling, handling temporal data \
**Tools/Programming Languages Used:** Python, Altair
**Co-author:** This was a class project done in collaboration with Neha Kardam, Mai Peng, Boyuan Xie

<hr>

We compared the performance of various machine learning models to automatically classify different music genres.

## Dataset

We used a subset of the Million song Dataset which consisted of 10 genres. We used a balanced training set of 40,000 songs and a balanced test set of 10,000 songs. Each song consisted of 3000 features. The features belonged to three main categories: timbre features, chroma features and loudness. 

## Summary

We first etablished baseline models for the classification task such as random classification, Gaussian Mixture Models and Support Vector Machines. We then implemented CNNs and CRNNs to do the same task. We found that both CNNs and CRNNs surpass the accuracy of baseline models, with CRNNs performing better than CNNs.
