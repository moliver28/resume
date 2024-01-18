---
layout: page
title: Sparse Transformer on FPGA
description: Microsoft internship project
img: /assets/img/microsoft.jpg
importance: 1
category: machine learning
---

# Problem

Microsoft's cloud-based platform for real-time AI serving, Brainwave, uses high-performance field-programmable gate arrays (FPGAs) to accelerate inferencing. Project Brainwave inferencing for services such as Bing and Azure. For this internship, my team, which served Bing wanted to know whether inferencing could be further accelerated by supporting sparse computations in Brainwave's BERT framework. To address this, I performed the following tasks:

- Analyzed the feasibility of supporting sparse computations within the Self Attention function of Brainwave's BERT framework.
- Designed, implement/modify, and test firmware to support sparse computations in BERT, ensuring seamless integration with the existing framework.
- Identified and suggest ways to extend the architecture to better support sparsity, thus improving the overall performance of the framework.

Through these tasks, I demonstrated the speed gains and latency reductions for the existing BERT framework if sparse computations were used. However, I also identified limitations that needed to be addressed before putting sparse computations into production.


<hr>
# What is BERT?
BERT is a pre-trained language model designed for various general natural language processing (NLP) tasks, including but not limited to question answering, next sentence prediction, and sequence classification. This versatile model can be fine-tuned for specific tasks, making it a valuable tool for a wide range of NLP applications.

<hr>

# Sparse Transformers

<img align="right" src="/assets/img/sparse.png" width= "400" height = "300">
The full transformer has limitations, particularly in terms of its memory and computational requirements, which increase quadratically as the sequence length grows. Sparse transformers refer to a variant of the transformer architecture that aims to reduce the computational complexity of the original model while maintaining or improving its performance. This is achieved by focusing on the most relevant parts of the input sequence, rather than processing the entire sequence at once. By using sparsity to limit the amount of information that needs to be processed, Sparse Transformers have shown promise in achieving state-of-the-art results on several natural language processing tasks with significantly reduced computation time and resource requirements.

<hr>

# Solution Approach
Brainwave performs computation in the form of tiles consisting of matrices of input. My approach was to modify the tile engine such that it performs computation only on the tiles that have values in it.

## Objectives

- Develop a method for computing only the tiles comprising the lower triangular half of the attention score matrix, thus reducing computational requirements.
- Implement this method for any given arbitrary sparse pattern, regardless of sequence length.
- Analyze the impact of different sparse patterns and their parameters (such as sequence length and window size) on the performance of the model.
- Explore hardware and architectural changes that could be made to the existing functionality to further leverage sparsity and accelerate attention computation.

## Results
The results of this project demonstrate:
- A significant decrease in latency when adding support for sparse computations to the attention mechanism. This decrease in latency is found to scale with sequence length and sparsity, indicating the potential for even greater improvements with larger and sparser datasets.

- Some anomalous behavior and overhead within the context computation needed further investigation to ensure optimal performance. 
- Packing dense tiles together has been identified as a means of saving VRF space, providing additional benefits in terms of resource utilization.

Overall, these results offer promising insights into the potential of sparse computations to improve the efficiency and effectiveness of natural language processing models, paving the way for further research and development in this area.

## Challenges

This project encountered several challenges related to supporting large sequence lengths in BERT:

- Limited memory in the BERT SKU makes it currently infeasible to support large sequence lengths.
- All testing was done in an emulator with unrealistic VRF sizes, which could impact the accuracy and performance of the model in real-world scenarios.
- The lack of a pre-trained model limited my ability to conduct a comprehensive analysis of the impact of increased sparsity on accuracy and model performance.

Addressing these challenges will require further research and development, including the exploration of new hardware solutions and the creation of more comprehensive testing environments to better evaluate the impact of sparsity on model accuracy and performance.

## Learnings
This project offered several valuable learnings:

- Modifying existing firmware to integrate a new model can be challenging but also rewarding and enjoyable.
- There may be a tradeoff between the robustness offered by sparse patterns and computational performance, which needs to be carefully considered when designing and implementing sparse transformers.
- The end-to-end process of breaking down a new model and porting it to hardware can be complex and challenging, but it provides a valuable engineering lesson on how to optimize performance and improve the efficiency of deep learning models on hardware platforms.
