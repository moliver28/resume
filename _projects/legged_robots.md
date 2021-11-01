---
layout: page
title: A Python Framework for Legged Robots
description: 
img:
importance: 3
category: technical
---

* Tools/Programming languages used: Python, MATLAB

In this project, I ported from MATLAB to Python, a computational framework for simulating two different models of legged hybrid systems: a passive dynamic biped and a bounding quadruped. 


<hr>

# Background 

Legged robotic systems usually fall under the category of hybrid dynamical systems. Hybrid dynamical systems can be thought of as a combination of properties of continuous and discrete
systems. In case of legged locomotion, when a foot/feet collide(s) with or leave(s) the ground, the continuous dynamics of the legged body are disrupted and need alteration. The instances when these disruptions occur are known as events.
The “jump map” dictates how the system will behave when an event occurs. The “jump set” (also known as the “guard set”) of the system determines when an event has occurred. The occurrence of an event is commonly characterized by a zero crossing of some state or function that is being monitored during simulation. The “flow map” directs the continuous dynamics of the system.

This project builds upon the MATLAB framework for legged systems as provided in [1] and attempts to convert it to Python. The advantages of Python over MATLAB are twofold.
Firstly, Python compilers are available on most operating systems, free of charge, unlike MATLAB. Secondly, Python code can run on microcontrollers such as the Beaglebone, and thus can directly be used to run on real robotic systems. Two
examples of legged systems were used in this project: the passive dynamic biped and the bounding quadruped. The former system as rightly named is passive and does not involve any actuation. The bounding quadruped on the other hand is
modeled as an activated system, where the activation function was obtained from [1] and [2]. The product of this project can be a tool to aid further reseach into legged systems with a Python based framework. 

<hr>

# Further reading

A detailed description and results of the project can be found <a href = "{{ site.baseurl }}/assets/pdf/546_Hybrid_System.pdf">here</a>
The code for the framework can be found <a href = "https://github.com/shruti-misra/Legged-Robots-Python">here</a>a>