---
title: Speech Recognition - Trigger Word Detection
tags: [Speech Recognition, CNN, Keras]
style: fill
color: secondary
description: My trigger word is "Activate". Every time it hears you say "activate," it will make a "chiming" sound.
---
In this assignment, my trigger word is "Activate". Every time it hears you say "activate," it will make a "chiming" sound.
The model will use 1-D convolutional layers, GRU layers, and dense layers, which can be imported from Keras. The following figure shows the detail of the model.
{% include elements/figure.html image="../assets/img/blogspeechreg.jpg" caption="iOS" %}

____________________________________________________________
Layer (type)                 Output Shape          Param #   
============================================================
input_1 (InputLayer)         (None, 5511, 101)     0         
____________________________________________________________
conv1d_1 (Conv1D)            (None, 1375, 196)     297136    
____________________________________________________________
batch_normalization_1 (Batch (None, 1375, 196)     784       
____________________________________________________________
activation_1 (Activation)    (None, 1375, 196)     0         
____________________________________________________________
dropout_1 (Dropout)          (None, 1375, 196)     0         
____________________________________________________________
gru_1 (GRU)                  (None, 1375, 128)     124800    
____________________________________________________________
dropout_2 (Dropout)          (None, 1375, 128)     0         
____________________________________________________________
batch_normalization_2 (Batch (None, 1375, 128)     512       
____________________________________________________________
gru_2 (GRU)                  (None, 1375, 128)     98688     
____________________________________________________________
dropout_3 (Dropout)          (None, 1375, 128)     0         
____________________________________________________________
batch_normalization_3 (Batch (None, 1375, 128)     512       
____________________________________________________________
dropout_4 (Dropout)          (None, 1375, 128)     0         
____________________________________________________________
time_distributed_1 (TimeDist (None, 1375, 1)       129       
============================================================
Total params: 522,561
Trainable params: 521,657
Non-trainable params: 904
 
Finally, the development set accuracy I got for the trigger word detection problem is 94.56%.

