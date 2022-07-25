# **Introduction**
Osteoarthritis is the most common form of arthritis, affecting millions of people worldwide. It occurs when the protective cartilage that cushions the ends of the bones wears down over time. Although osteoarthritis can damage any joint, the disorder most commonly affects joints in your hands, knees, hips and spine. This model will attemp to find a solution for the easy detection of knee Osteoarthritis
# **About the Dataset**
## Osteoarthritis Knee X-ray
[Dataset Link](https://www.kaggle.com/datasets/shashwatwork/knee-osteoarthritis-dataset-with-severity)\
\
https://www.kaggle.com/datasets/shashwatwork/knee-osteoarthritis-dataset-with-severity
Dataset contains knee xray images, which are preprocessed and edited to easily detect the knee.  
![image](https://user-images.githubusercontent.com/100197432/180833493-c4b5b20a-3c0c-4fef-8fd9-d4d1219351cd.png)
# **About CNNS**
![image](https://user-images.githubusercontent.com/100197432/180833662-492d6fa9-efc2-4baf-855f-f8010a20d3f7.png)  
Convolutional Neural Network is a Deep Learning algorithm which can take in an input image, assign importance in the form of learnable weights and biases to various aspects/objects in the image and be able to differentiate one from the other. The pre-processing required in a CNN is much lower as compared to other classification algorithms. While in primitive methods filters are hand-engineered, with enough training, the role of the CNN is to reduce the images into a form which is easier to process, without losing features which are critical for getting a good prediction have the ability to learn these filters/characteristics.  
![image](https://user-images.githubusercontent.com/100197432/180833795-107757a4-47c4-48f0-8ec4-61e4e6ca9e56.png)  
It contains 3 types of layers, \
\
A convolutional layer, which is the main building block of a CNN. It contains a set of filters, parameters of which are to be learned throughout the training. The size of the filters is usually smaller than the actual image. Each filter convolves with the image and creates an activation map.  
![image](https://user-images.githubusercontent.com/100197432/180833966-84354c51-78e7-4128-9c92-4b9e1495c636.png)
A Pooling layer used to reduce the dimensions of the feature maps. Thus, it reduces the number of parameters to learn and the amount of computation performed in the network. The pooling layer summarizes the features present in a region of the feature map generated by a convolution layer  
![image](https://user-images.githubusercontent.com/100197432/180834034-47a1bdfc-bf02-490d-bf28-1484d7ec94ac.png)  
A fully connected layer that multiplies the input by a weight matrix and then adds a bias vector, However GlobalAveragePooling eliminates the need for this layer  
![image](https://user-images.githubusercontent.com/100197432/180834083-aac266cd-3879-4a7b-a366-0d761eb2472a.png)   
## Models Used
### Generic
### Numpy
Numpy is a general-purpose array-processing package. It provides a high-performance multidimensional array object, and tools for working with these arrays. It is the fundamental package for scientific computing with Python.Besides its obvious scientific uses, Numpy can also be used as an efficient multidimensional container of generic data.

### Pandas
Pandas is an open-source library that is built on top of NumPy library.It is a Python package that offers various data structures and operations for manipulating numerical data and time series. It is mainly popular for importing and analyzing data much easier. Pandas is fast and it has highperformance & productivity for users.

### Matplotlib
Matplotlib is an visualization library in Python for 2D plots of arrays. Matplotlib is a multi-platform data visualization library built on NumPy arrays and designed to work with the broader SciPy stack. It was introduced by John Hunter in the year 2002. One of the greatest benefits of visualization is that it allows us visual access to huge amounts of data in easily digestible visuals. Matplotlib consists of several plots like line, bar, scatter, histogram etc.

### Seaborn
Seaborn is an visualization library for statistical graphics plotting in Python. It provides beautiful default styles and color palettes to make statistical plots more attractive. It is built on the top of matplotlib library and also closely integrated to the data structures from pandas. Seaborn aims to make visualization the central part of exploring and understanding data. It provides dataset-oriented APIs, So that we can switch between different visual representations for same variables for better understanding of dataset.

### Os
The OS module in Python provides functions for interacting with the operating system. OS comes under Python’s standard utility modules. This module provides a portable way of using operating system-dependent functionality. The os and os.path modules include many functions to interact with the file system.

### Sci-Kit Learn
Confusion Matrix
Confusion matrix are used to evaluate the quality of the output of a classifier on dataset. The diagonal elements represent the number of points for which the predicted label is equal to the true label, while off-diagonal elements are those that are mislabeled by the classifier. The higher the diagonal values of the confusion matrix the better, indicating many correct predictions.

### Class Weights
In cases where data is unbalanced, weights need to be estimated. compute_sample_weight estimates the sample weights by class for unbalanced datasets whereas compute_class_weight estimate class weights for unbalanced datasets.

### CNN
Tensorflow
TensorFlow is an end-to-end open source platform for machine learning. It has a comprehensive, flexible ecosystem of tools, libraries and community resources that lets researchers push the state-of-the-art in ML and developers easily build and deploy ML powered applications. TensorFlow provides a collection of workflows to develop and train models using Python or JavaScript, and to easily deploy in the cloud, on-prem, in the browser, or on-device no matter what language you use. The tf. data API enables you to build complex input pipelines from simple, reusable pieces.

### Keras
Keras is a deep learning API written in Python, running on top of the machine learning platform TensorFlow. It was developed with a focus on enabling fast experimentation. Being able to go from idea to result as fast as possible is key to doing good research. Keras reduces developer cognitive load, adopts the principle of progressive disclosure of complexity: simple workflows should be quick and easy, while arbitrarily advanced workflows should be possible via a clear path that builds upon what you've already learned.Keras provides industry-strength performance and scalability.

### Layers
#### Conv2D
This layer creates a convolution kernel that is convolved with the layer input to produce a tensor of outputs. If use_bias is True, a bias vector is created and added to the outputs. Finally, if activation is not None, it is applied to the outputs as well.

#### SeparableConv2D
Separable convolutions consist of first performing a depthwise spatial convolution (which acts on each input channel separately) followed by a pointwise convolution which mixes the resulting output channels. The depth_multiplier argument controls how many output channels are generated per input channel in the depthwise step. Intuitively, separable convolutions can be understood as a way to factorize a convolution kernel into two smaller kernels, or as an extreme version of an Inception block.

#### BatchNormalization
Batch normalization applies a transformation that maintains the mean output close to 0 and the output standard deviation close to 1. Importantly, batch normalization works differently during training and during inference. During training, the layer normalizes its output using the mean and standard deviation of the current batch of inputs. That is to say, for each channel being normalized, the layer returns (gamma * (batch - mean(batch)) / sqrt(var(batch) + epsilon) + beta) Where

*Epsilon is small constant (configurable as part of the constructor arguments)\
*Gamma is a learned scaling factor (initialized as 1), which can be disabled by passing scale=False to the constructor.\
*Beta is a learned offset factor (initialized as 0), which can be disabled by passing center=False to the constructor.
#### MaxPooling2D
Downsamples the input along its spatial dimensions (height and width) by taking the maximum value over an input window (of size defined by pool_size) for each channel of the input. The window is shifted by strides along each dimension.

The resulting output, when using the "valid" padding option, has a spatial shape (number of rows or columns) of: output_shape = math.floor((input_shape - pool_size) / strides) + 1 (when input_shape >= pool_size)

#### GlobalAveragePooling2D
Global Average Pooling is a pooling operation designed to replace fully connected layers in classical CNNs. The idea is to generate one feature map for each corresponding category of the classification task in the last mlpconv layer. Instead of adding fully connected layers on top of the feature maps, we take the average of each feature map, and the resulting vector is fed directly into the softmax layer. It is more native to the convolution structure by enforcing correspondences between feature maps and categories. Thus the feature maps can be easily interpreted as categories confidence maps. There is no parameter to optimize in the global average pooling thus overfitting is avoided at this layer. Furthermore, global average pooling sums out the spatial information, thus it is more robust to spatial translations of the input.

#### Activation
An activation function is the last component of the convolutional layer to increase the non-linearity in the output.

*Relu
ReLU stands for rectified linear unit, and is a type of activation function. Mathematically, it is defined as y = max(0, x) ReLU is linear (identity) for all positive values, and zero for all negative values.
*Softmax
Softmax converts a vector of values to a probability distribution. The elements of the output vector are in range (0, 1) and sum to 1. Each vector is handled independently. The axis argument sets which axis of the input the function is applied along. Softmax is often used as the activation for the last layer of a classification network because the result could be interpreted as a probability distribution.The input values in are the log-odds of the resulting probability.
*Adam
The Adam optimization algorithm is an extension to stochastic gradient descent. Stochastic gradient descent maintains a single learning rate (termed alpha) for all weight updates and the learning rate does not change during training. A learning rate is maintained for each network weight (parameter) and separately adapted as learning unfolds.
## Conclusion
With a validation accuracy of around 94% and a testing accuracy of 97%, the model seems to do well in categorizing medical images from 5 different classes. Out of all models attempted, CNN seemt to be the most accurate in classifying the x-ray images. We can observe how CNNs are very good at certain tasks, especially recognizing objects in pictures and videos, and how we can train a model for multiclass classification
