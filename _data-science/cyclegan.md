---
layout: page
title: CycleGANs for Generating Realistic Depth Map Data
description: 
img: /assets/img/CycleGANs.JPG
importance: 5
category: machine learning
---

**Concepts Learned:** Generative Adversarial Networks (GANs) \
**Tools/Programming languages used:** Python, Keras \
**Project Type:** Class Project
**Team:** Kyle Lindgren, **Shruti Misra**

<hr>

# The Setting

Advancement of recent technologies such as augmented reality systems relies on understanding scene geometry, which requires accurate depth map training data. However,
it is difficult and time consuming to physically collect high quality depth maps from commercial cameras such as the Microsoft Kinect and IntelSense. Therefore, the idea of training on synthetic instead of real images is appealing because data collection is much easier, faster and less expensive. However, learning from synthetic data can be complicated, due to a gap between synthetic and real data distributions. Therefore, a network trained on synthetic data might not generalize well to real images. Moreover, adding "realism to synthetically generated data is computationally expensive and does not always capture the nuances of real images.

We attempted to use CycleGANs to generate realistic depth map data, where the goal is to produce realistic depth images from synthetic ones, by mapping unpaired real depth images from a camera to synthetically rendered images and vice versa.The main appeal of CycleGANs is their ability to use unpaired data to learn. Pairs of real depth maps from cameras and their synthetically rendered counterparts are difficult to obtain and generate. Since, most of the GAN research in this domain uses paired data, CycleGAN stand out in this somewhat unique capability.

# The Dataset

The dataset used for this application was the NYU hand pose dataset, which contains 72,757 training frames and 8,251 testing frames for each of three poses captured by Kinect v1 cameras. Depth frames are labeled with hand pose information which has been used to create synthetic depth images within an OpenGL-based framework. For this work, the depth samples with the hand region were extracted, reducing the image size to 128x128, effectively reducing the number of training parameters and training times.

# Results

<p style="text-align:center;"><img src="{{ site.baseurl }}/assets/img/CycleGANs.JPG" height= "400" width = "400"></p>

Qualitatively, from Figure 1 it can be observed that the realistic data "looks" similar to the real data from the NYU dataset. This shows that the trained network learned, with reasonable amount of accuracy, the high level noise model observed by Kinect v1 depth sensors; the real depth camera utilized in the training dataset of real images. The MSE value computed between the real data X and the output data  was 5523.81.

# Some Findings

Initially, this project was intended to use CycleGAN for depth map inpainting. The problem of inpainting in depth maps is a difficult one to solve due to lack of strong features in depth maps as opposed to color images. GAN methods exist for color image inpainting, but not so much for depth maps. Therefore, when the CycleGAN was trained on two different real and synthetic datasets and applied the ‘real2synth’ generator to noised, real images from a third dataset , the in-painting process failed. Through this project, it was realized that while being able to mimic different distributions of data, CycleGANs might often be unable to learn information
that is not strongly present in the training data and further generalize it to different datasets. This makes CycleGANs of limited use when trying to generate new information, instead of correlating different renderings.

