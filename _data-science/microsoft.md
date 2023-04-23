---
layout: page
title: Sparse Transformer on FPGA
description: Microsoft internship project
img: /assets/img/food.jpg
importance: 1
category: machine learning
---

# Goal

The primary goals of this internship were to assess the feasibility of supporting sparse computations in Brainwave's BERT framework. To achieve these objectives, the following tasks were performed:

- Analyze the feasibility of supporting sparse computations within the Self Attention function of Brainwave's BERT framework.
- Design, implement/modify, and test firmware to support sparse computations in BERT, ensuring seamless integration with the existing framework.
- Identify and suggest ways to extend the architecture to better support sparsity, thus improving the overall performance of the framework.

Through these tasks, we aimed to enhance the capabilities of Brainwave's BERT framework, ultimately improving its efficiency and effectiveness in handling sparse computations.

<hr>

# What is Brainwave?
Microsoft's cloud-based platform for real-time AI serving, Brainwave, offers accelerated deep neural network (DNN) inferencing powered by high-performance field-programmable gate arrays (FPGAs). This advanced technology enables the platform to perform complex computations efficiently, making it a valuable tool for deep learning applications. Project Brainwave currently serves DNNs in real
time for production services such as Bing and Azure

<hr>
# What is BERT?
BERT is a pre-trained language model designed for various general natural language processing (NLP) tasks, including but not limited to question answering, next sentence prediction, and sequence classification. This versatile model can be fine-tuned for specific tasks, making it a valuable tool for a wide range of NLP applications. The BaseBERT model performs approximately 2,097,152 floating point matrix-vector multiplication operations.
These multiplication ops form the bulk of the high latency computations performed on the FPGA.

<hr>

# Sparse Transformers
The full transformer has limitations, particularly in terms of its memory and computational requirements, which increase quadratically as the sequence length grows. sparse transformers refer to a variant of the transformer architecture that aims to reduce the computational complexity of the original model while maintaining or improving its performance. This is achieved by focusing on the most relevant parts of the input sequence, rather than processing the entire sequence at once. By using sparsity to limit the amount of information that needs to be processed, Sparse Transformers have shown promise in achieving state-of-the-art results on several natural language processing tasks with significantly reduced computation time and resource requirements.

<hr>

#Incorporating Sparsity into Brainwave: Approach
Brainwave performs computation in the form of tiles consisting of matrices of input. My approach was to modify the tile engine such that it performs computation only on the tiles that have values in it.

## Objectives

- Develop a method for computing only the tiles comprising the lower triangular half of the attention score matrix, thus reducing computational requirements.
- Implement this method for any given arbitrary sparse pattern, regardless of sequence length.
- Analyze the impact of different sparse patterns and their parameters (such as sequence length and window size) on the performance of the model.
- Explore hardware and architectural changes that could be made to the existing functionality to further leverage sparsity and accelerate attention computation.
