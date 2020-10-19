---
title: Using Keras to build 50-layer Residual Networks for Image Recognition
tags: [CNN, Keras]
style: fill
color: info
description: the ResNet model with 50 layers
---
Keras was developed to enable deep learning engineers to build and experiment with different models very quickly. Just as TensorFlow is a higher-level framework than Python, Keras is an even higher-level framework and provides additional abstractions. Being able to go from idea to result with the least possible delay is key to finding good models. However, Keras is more restrictive than the lower-level frameworks, so there are some very complex models that you can implement in TensorFlow but not (without more difficulty) in Keras. That being said, Keras will work fine for many common models.
In this assignment, I built ResNet model with 50 layers. The following figure describes in detail the architecture of this neural network.
{% include elements/figure.html image="../assets/img/blogusingkeras.jpg" caption="iOS" %}

The details of this ResNet-50 model are:
-	Zero-padding pads the input with a pad of (3,3)
-	Stage 1:
1	The 2D Convolution has 64 filters of shape (7,7) and uses a stride of (2,2). Its name is "conv1".
2	BatchNorm is applied to the channels axis of the input.
3	MaxPooling uses a (3,3) window and a (2,2) stride.
-	Stage 2:
1	The convolutional block uses three set of filters of size [64,64,256], "f" is 3, "s" is 1 and the block is "a".
2	The 2 identity blocks use three set of filters of size [64,64,256], "f" is 3 and the blocks are "b" and "c".
-	Stage 3:
-	The convolutional block uses three set of filters of size [128,128,512], "f" is 3, "s" is 2 and the block is "a".
-	The 3 identity blocks use three set of filters of size [128,128,512], "f" is 3 and the blocks are "b", "c" and "d".
-	Stage 4:
-	The convolutional block uses three set of filters of size [256, 256, 1024], "f" is 3, "s" is 2 and the block is "a".
-	The 5 identity blocks use three set of filters of size [256, 256, 1024], "f" is 3 and the blocks are "b", "c", "d", "e" and "f".
-	Stage 5:
1	The convolutional block uses three set of filters of size [512, 512, 2048], "f" is 3, "s" is 2 and the block is "a".
2	The 2 identity blocks use three set of filters of size [256, 256, 2048], "f" is 3 and the blocks are "b" and "c".
-	The 2D Average Pooling uses a window of shape (2,2) and its name is "avg_pool".
-	The flatten doesn't have any hyperparameters or name.
-	The Fully Connected (Dense) layer reduces its input to the number of classes using a softmax activation. Its name should be 'fc' + str(classes).
After building the ResNet model, we can import any dataset for some image recognition.

