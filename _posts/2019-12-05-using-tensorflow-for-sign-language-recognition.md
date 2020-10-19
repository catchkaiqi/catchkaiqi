---
title: Using TensorFlow for Sign Language Recognition
tags: [TensorFlow, CNN]
style: fill
color: light
description:
---

This practical application of deep learning is built using programming frameworks, which have many built-in functions I can simply call.
The model I built here is the model: CONV2D -> RELU -> MAXPOOL -> CONV2D -> RELU -> MAXPOOL -> FLATTEN -> FULLYCONNECTED.
Here are the following parameters for all the steps in detail:
 - Conv2D: stride 1, padding is "SAME"
 - ReLU
 - Max pool: Use an 8 by 8 filter size and an 8 by 8 stride, padding is "SAME"
 - Conv2D: stride 1, padding is "SAME"
 - ReLU
 - Max pool: Use a 4 by 4 filter size and a 4 by 4 stride, padding is "SAME"
 - Flatten the previous output.
 - FULLYCONNECTED (FC) layer: Apply a fully connected layer without an non-linear activation function. Do not call the softmax here. This will result in 6 neurons in the output layer, which then get passed later to a softmax. In TensorFlow, the softmax and cost function are lumped together into a single function, which you'll call in a different function when computing the cost. 
{% include elements/figure.html image="../assets/img/blogusingtens.jpg" caption="iOS" %}

