---
title: Methods to Improve Neural Network Performance
tags: [NN, regularization, dropout, optimization]
style: fill
color: secondary
description: Several ways such as good initialization, gradient checking, regularization, and different optimization methods to improve neural network performance.
---

There are several ways such as good initialization, gradient checking, regularization, and different optimization methods to improve neural network performance.
-	A well-chosen initialization can:
1	Speed up the convergence of gradient descent
2	Increase the odds of gradient descent converging to a lower training (and generalization) error
¥	Here are the three initialization methods:
1	Zeros initialization -- setting initialization = "zeros" in the input argument.
2	Random initialization -- setting initialization = "random" in the input argument. This initializes the weights to large random values. 
3	He initialization -- setting initialization = "he" in the input argument. This initializes the weights to random values scaled according to a paper by He et al., 2015.
After trying three different types of initializations. For the same number of iterations and same hyperparameters the comparison is:
{% include elements/figure.html image="../assets/img/blogmethodsto.jpg" caption="iOS" %}

Gradient checking method verifies closeness between the gradients from backpropagation and the numerical approximation of the gradient (computed using forward propagation). Since Gradient checking is slow, so we don't run it in every iteration of training. We usually run it only to make sure the code is correct, then turn it off and use backpropagation for the actual learning process.
{% include elements/figure.html image="../assets/img/blogmethodsto1.jpg" caption="iOS" %}

Gradient Checking, at least as we've presented it, doesn't work with dropout. We would usually run the gradient check algorithm without dropout to make sure your backpropagation is correct, then add dropout.

To reduce overfitting of the model, we added regularization terms. In this case, I compared the performances of a 3-layer neural network model without regularization, with L2 regularization, and dropout.
-	L2 Regularization
{% include elements/figure.html image="../assets/img/blogmethodsto2.jpg" caption="iOS" %}

-	 Dropout is a widely used regularization technique, it randomly shuts down some neurons in each iteration. Deep learning frameworks like tensorflow, PaddlePaddle, keras or caffe come with a dropout layer implementation.
Note that regularization hurts training set performance! This is because it limits the ability of the network to overfit to the training set. But since it ultimately gives better test accuracy, it is helping your system.
{% include elements/figure.html image="../assets/img/blogmethodsto3.jpg" caption="iOS" %}

For the optimization methods, we compare the performances using Batch Gradient Descent, Mini-Batch Gradient descent, Momentum, and Adam optimizations.
A simple optimization method in machine learning is gradient descent (GD). When we take gradient steps with respect to all examples on each step, it is also called Batch Gradient Descent. A variant of this is Stochastic Gradient Descent (SGD), which is equivalent to mini-batch gradient descent where each mini-batch has just 1 example.
{% include elements/figure.html image="../assets/img/blogmethodsto4.jpg" caption="iOS" %}

{% include elements/figure.html image="../assets/img/blogmethodsto5.jpg" caption="iOS" %}

-	Momentum stores the 'direction' of the previous gradients in the variable. Formally, this will be the exponentially weighted average of the gradient on previous steps.
{% include elements/figure.html image="../assets/img/blogmethodsto6.jpg" caption="iOS" %}

for l = 1,..., L
where L is the number of layers, beta is the momentum and alpha is the learning rate. All parameters should be stored in the parameters dictionary. Note that the iterator l starts at 0 in the for loop while the first parameters are W[l]  and b[l] (that's a "one" on the superscript).
The larger the momentum beta is, the smoother the update because the more we take the past gradients into account. But if it is too big, it could also smooth out the updates too much. Common values for beta range from 0.8 to 0.999. If you don't feel inclined to tune this,  is often a reasonable default.

-	Adam optimization
{% include elements/figure.html image="../assets/img/blogmethodsto7.jpg" caption="iOS" %}

The summary of three optimizations is in the following chart. Adam outperforms mini-batch gradient descent and Momentum. If we run the model for more epochs on this simple dataset, all three methods will lead to very good results. However, we will see that Adam converges a lot faster.
{% include elements/figure.html image="../assets/img/blogmethodsto8.jpg" caption="iOS" %}
