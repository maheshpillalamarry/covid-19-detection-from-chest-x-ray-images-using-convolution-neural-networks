# covid-19 detection from chest x-ray images using convolution neural networks



The goals of this project are threefold: 
- [1]               To explore development of a machine learning algorithm to distinguish chest X-rays of individuals with respiratory illness testing positive for COVID-19 from other X-rays,
- [2]               To promote discovery of patterns in such X-rays via CNN interpretability algorithms, and
- [3]               To build more robust and extensible machine learning infrastructure trained on a variety of data types, to aid in the global response to COVID-19.
- [4]               To achive best Accuracy.


## install:
* ### Python 3.6
    * recommend installing Anaconda as it is already set up for machine learning
    * Or else use Google's Colab with all libraries installed
* ### Libraries Required
    *  Kearas 
        * Keras is an open-source neural-network library written in Python. It is capable of running on top of TensorFlow, Microsoft Cognitive Toolkit, R, Theano, or PlaidML. Designed to enable fast experimentation with deep neural networks,   
    *  TensorFlow
        * TensorFlow is an open source library for numerical computation and large-scale machine learning. TensorFlow bundles together a slew of machine learning and deep learning (aka neural networking) models 
    *  Mathplotlib
        * Matplotlib is a plotting library for the Python programming language and its numerical mathematics extension NumPy.
    *  pandas
        * pandas is a software library written for the Python programming language for data manipulation and analysis.
    *  sklearn.metrics
        * The sklearn. metrics module implements several loss, score, and utility functions to measure classification performance
    *  seaborn
        * To visualize confusion matrix

## DataSet:
* #### Covid-19 chest x-ray images are obtained at 
    * https://github.com/ieee8023/covid-chestxray-dataset/tree/master/images
    
* #### Normal Images:(Extract the normal images from below dataset)
    * https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia 

## PROCEDURE
* Label the data from different data sets.
* Divide the data set into 80% for training and 20% for validation(Testing).
* choose the number of kernals(filters) and size of filters(3x3 standard).
* choose number of convolution layers needed and activation function(we uses relu).
* choose dense layers,optimizer and Test the data.
* find the Accuracy of the model.
* plot accuracy and loss of model.
* Compute confusion matrix to evaluate the accuracy of a classification.


# Block Diagram:
<img src="/blockdiagram/blockdiagram1.PNG" data-canonical-src="/blockdiagram/blockdiagram1.PNG " width="800" height="350" />



# Convolution Layer
* In which we apply the filter to a single position of the input. This will be used to build a convolutional unit, which:
    * Takes an input volume
    * Applies a filter at every position of the input
    * Outputs another volume (usually of different size)
<img src="https://media.giphy.com/media/i4NjAwytgIRDW/giphy.gif" data-canonical-src="https://media.giphy.com/media/i4NjAwytgIRDW/giphy.gif "/>

* In a computer vision application, each value in the matrix on the left corresponds to a single pixel value, and we convolve a 3x3 filter with the image by multiplying its values element-wise with the original matrix, then summing them up and adding a bias. In this first step of the exercise, you will implement a single step of convolution, corresponding to applying a filter to just one of the positions to get a single real-valued output.
  
# Max Pooling

* The pooling (POOL) layer reduces the height and width of the input. It helps reduce computation, as well as helps make feature detectors more invariant to its position in the input. The two types of pooling layers are:
    * Max-pooling layer: slides an (f,f) window over the input and stores the max value of the window in the output.
<img src="https://hackernoon.com/hn-images/1*Feiexqhmvh9xMGVVJweXhg.gif" data-canonical-src="https://hackernoon.com/hn-images/1*Feiexqhmvh9xMGVVJweXhg.gif" width="600" height="250" />


