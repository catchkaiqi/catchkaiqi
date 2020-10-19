---
title: Building Face Recognition System Using FaceNet Neural Network
tags: [FaceNet, CNN]
style: border
color: primary
description: Face Verification & Face Recognition
---
Face recognition problems commonly fall into two categories:
-	Face Verification - "is this the claimed person?". For example, at some airports, you can pass through customs by letting a system scan your passport and then verifying that you (the person carrying the passport) are the correct person. A mobile phone that unlocks using your face is also using face verification. This is a 1:1 matching problem. 
-	Face Recognition - "who is this person?". For example, when employees enter the office without needing to otherwise identify themselves. This is a 1:K matching problem.
The FaceNet learns a neural network (Inception model) that encodes a face image into a vector of 128 numbers. It is pretrained and we can just define the cost function and load the weights. 
For Face Verification, I compared the distance of two vectors to determine if two pictures are of the same person.
{% include elements/figure.html image="../assets/img/blogbuildingface.jpg" caption="iOS" %}
So, an encoding is a good one if:
1	The encodings of two images of the same person are quite similar to each other 
2	The encodings of two images of different persons are very different
For Face Recognition, I implemented a system that takes as input an image, and figures out if it is one of the authorized persons (and if so, who). Unlike the previous face verification system, we will no longer get a person's name as another input.
This function computes the target encoding of the image and loops over the database dictionary's names and encodings to compute L2 distance between the target "encoding" and the current "encoding" from the database. If the distance is less than min_dist, then set min_dist to dist, and identity to name.
 
Here're some ways to further improve the algorithm:
-	Put more images of each person (under different lighting conditions, taken on different days, etc.) into the database. Then given a new image, compare the new face to multiple pictures of the person. This would increae accuracy.
-	Crop the images to just contain the face, and less of the "border" region around the face. This preprocessing removes some of the irrelevant pixels around the face, and also makes the algorithm more robust.
 
1	Face verification solves an easier 1:1 matching problem; face recognition addresses a harder 1:K matching problem. 
2	The triplet loss is an effective loss function for training a neural network to learn an encoding of a face image.
3	The same encoding can be used for verification and recognition. Measuring distances between two images' encodings allows you to determine whether they are pictures of the same person. 
 
REFERENCES:
-	Florian Schroff, Dmitry Kalenichenko, James Philbin (2015). FaceNet: A Unified Embedding for Face Recognition and Clustering
-	Yaniv Taigman, Ming Yang, Marc'Aurelio Ranzato, Lior Wolf (2014). DeepFace: Closing the gap to human-level performance in face verification
-	The pretrained model we use is inspired by Victor Sy Wang's implementation and was loaded using his code: https://github.com/iwantooxxoox/Keras-OpenFace.
Our implementation also took a lot of inspiration from the official FaceNet github repository: https://github.com/davidsandberg/facenet
