---
title: Using Word Vector Representations to Build an Emojifier
tags: [Word Vector, LSTM]
style: fill
color: danger
description: a sophisticated model (Emojifier-V2) that incorporates an LSTM neural network
---
Using word vectors, even if my training set explicitly relates only a few words to a particular emoji, the algorithm will be able to generalize and associate words in the test set to the same emoji even if those words don't even appear in the training set. This allows us to build an accurate classifier mapping from sentences to emojis, even using a small training set.
In this assignment, I built a sophisticated model (Emojifier-V2) that incorporates an LSTM neural network. Here is the overview of the model.
{% include elements/figure.html image="../assets/img/blogusingword.jpg" caption="iOS" %}

____________________________________________________________Layer (type)                 Output Shape          Param #   
============================================================
input_1 (InputLayer)         (None, 10)            0         
____________________________________________________________
embedding_2 (Embedding)      (None, 10, 50)        20000050  
____________________________________________________________
lstm_1 (LSTM)                (None, 10, 128)       91648     
____________________________________________________________
dropout_1 (Dropout)          (None, 10, 128)       0         
____________________________________________________________
lstm_2 (LSTM)                (None, 128)           131584    
____________________________________________________________
dropout_2 (Dropout)          (None, 128)           0         
____________________________________________________________
dense_1 (Dense)              (None, 5)             645       
____________________________________________________________
activation_1 (Activation)    (None, 5)             0         
============================================================
Total params: 20,223,927
Trainable params: 223,877
Non-trainable params: 20,000,050
Finally, I got a test accuracy between 80% and 95%. If the training set were larger, the LSTM model would be much better than at understanding such complex sentences.



