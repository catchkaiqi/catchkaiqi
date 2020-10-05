---
title: Cat vs Non-cat Image Classification 
tags: [Classification, Neural Network]
style: fill
color: warning
description: an L-layer deep neural network for image classification
---
 
In this assignment, I built an L-layer deep neural network for image classification. For here, L can be any integer greater than 0. In this case, I picked L as 5 and achieved training accuracy as 100% and test accuracy as 84% to differentiate cat and non-cat images.
Here is the representation of an L-layer deep neural network.
{% include elements/figure.html image="../assets/img/neuralnetworkrep.jpg" caption="iOS" %}
{% include elements/figure.html image="../assets/img/neuralnetworkrep2.jpg" caption="iOS" %}

The general deep learning methodology to build the model is as the following:
1. Initialize parameters / Define hyperparameters
2. Loop for num_iterations:
    a. Forward propagation
    b. Compute cost function
    c. Backward propagation
    d. Update parameters (using parameters, and grads from backprop) 
4. Use trained parameters to predict labels
Here is the output of the cross-entropy cost after 2400 iterations.

{% include elements/figure.html image="../assets/img/blogcatresult.jpg" caption="iOS" %}

The 5-layer neural network has test accuracy (84%) than your 2-layer neural network (72%) on the same test set.
Here is an example testing with a cat image.

{% include elements/figure.html image="../assets/img/blogcattestimg.jpg" caption="iOS" %}
