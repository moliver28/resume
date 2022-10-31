---
layout: page
title: Machine learning models for music genre classification
description: 
img: /assets/img/genre.gif
importance: 2
category:machine learning
---

**Concepts learned:** Gaussian mixture models, Support Vector Machines (SVMs), Convolutional Recurrent Neural Networks (RNN), Convolutional Neural Networks (CNN) \
**Co-author:** This was a class project done in collaboration with Manuja Sharma 

<hr>

We compared the performance of various machine learning models to automatically classify different music genres.

## Dataset

We used a subset of the Million song Dataset which consisted of 10 genres. We used a balanced training set of 40,000 songs and a balanced test set of 10,000 songs. Each song consisted of 3000 features. The features belonged to three main categories: timbre features, chroma features and loudness. 

## Summary

We first etablished baseline models for the classification task such as random classification, Gaussian Mixture Models and Support Vector Machines. We then implemented CNNs and CRNNs to do the same task. We found that both CNNs and CRNNs surpass the accuracy of baseline models, with CRNNs performing better than CNNS.
