---
title: Autonomous driving - Car detection by YOLO Model
tags: [YOLO, CNN]
style: fill
color: dark
description:  The critical component of a self-driving car project is building a car detection system. 
---
The critical component of a self-driving car project is building a car detection system. 
{% include elements/figure.html image="../assets/img/blogautonomous.jpg" caption="iOS" %}

To collect data, we've mounted a camera to the hood (meaning the front) of the car, which takes pictures of the road ahead every few seconds while you drive around. After gathering all these images into a folder, we labeled them by drawing bounding boxes around every car we found as the figure on the left.
YOLO ("you only look once") is a popular algorithm because it achieves high accuracy while also being able to run in real-time. This algorithm "only looks once" at the image in the sense that it requires only one forward propagation pass through the network to make predictions. After non-max suppression, it then outputs recognized objects together with the bounding boxes.
There is an existing pretrained Keras YOLO model stored in "yolo.h5". (These weights come from the official YOLO website, and were converted using a function written by Allan Zelener.
{% include elements/figure.html image="../assets/img/blogautonomous1.jpg" caption="iOS" %}


