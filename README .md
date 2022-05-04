
# Fake News Detection using Deep Learning

## Overview:
Fake news's simple meaning is to incorporate information that leads people to the wrong path.By practicing this advanced python project of detecting fake news, you will easily make a difference between real and fake news.

## Prerequisites:
1. python
2. You will also need to download and install the required packages after you install :
+ Keras
+ Tensorflow
+ Numpy
+ Pandas
+ Scikit-learn
+ Seaborn
+ NLTK

## Dataset:
The Dataset is collected from Kaggle (https://www.kaggle.com/)

## One Hot Representation:
One Hot Encoding is a common way of preprocessing categorical features for machine learning models. This type of encoding creates a new binary feature for each possible category and assigns a value of 1 to the feature of each sample that corresponds to its original category. 

## Word Embedding:
It is an approach for representing words and documents. Word Embedding or Word Vector is a numeric vector input that represents a word in a lower-dimensional space. It allows words with similar meaning to have a similar representation. They can also approximate meaning. A word vector with 50 values can represent 50 unique features.
+ How are Word Embeddings used?
1. They are used as input to machine learning models.
2. Take the words —-> Give their numeric representation —-> Use in training or inference
3. To represent or visualize any underlying patterns of usage in the corpus that was used to train them.

## LSTM for Text Classification in Python:
We define a sequential model and add various layers to it.
The first layer is Embedding layer. It representing words using a dense vector representation. The position of a word within the vector space is based on the words that surround the word when it is used.The next layer is an LSTM layer with 128 neurons. “embedded_docs” is the input list of sentences which is one hot encoded and every sentence is made of the same length. The activation function is rectified linear, which widely used. Any other relevant activation function can be used. “return_sequences=True” this is an important parameter while using multiple LSTM layer as it enables the output of the previous LSTM layer to be used as an input to the next LSTM layer. If it is not set to true, the next LSTM layer will not get the input.
The final Dense layer is the output layer which has 4 cells representing the 4 different categories in this case. The number can be changed according to the number of categories.
Compiling the model using adam optimizer and sparse_categorical_crossentropy. Adam optimizer is the current best optimizer for handling sparse gradients and noisy problems. The sparse_categorical_crossentropy is mostly used when the classes are mutually exclusive, ie, when each sample belongs to exactly one class.