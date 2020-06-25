# Neural Networks and Deep Learning  
**deeplearning.ai** 
Instructor: [Andrew Ng](http://www.andrewng.org/)
<BR>

### Course Outline

Week 1: Introduction  
Week 2: Basics of Neural Network Programming  
Week 3: One Hidden Layer Neural Networks  
Week 4: Deep Neural Networks  

### Week 1

#### Introduction to Deep Learning

Deep learning means training neural networks.
Simple linear regression is the most basic neural network, with the node being the regression equation having an input and output.

Advertising, image processing, and language processing are some of th biggest applications.
Image applications often use convolutional neural networks (CNN).
Sequence data (time series) often use recurring neural networks (RNN).
Data table is structured data, while image/audio is unstructured data.

Traditional learning algorithms plateau in performance, while neural networks continue to perform better as amount of data increases.
Scale drives deep learning progress.
Switch from using sigmoid functions to ReLU functions for deep learning increases speed of gradient descent significantly.

### Week 2

#### Logistic Regression as a Neural Network

Normally in deep learning you take a forward and backward propogation pass.
First step is to convert the three matrices representing an image into one feature vector x.
Multiple images are converted then stacked into a matrix X with each image as a column, this forms one part of the training data set.
The same is done with y, however, this results in a matrix with one row of (0,1).

In logistic regression y is equal to the sigmoid function of wTx + b. The sigmoid function of the standard linear regression model.

<p align="center">
<img src="https://github.com/peterhall71/coursera_Neural_Networks_and_Deep_Learning/blob/master/images/sigmoid_function.png" alt="Sigmoid Function" width="400"/>
</p>
<p align="center">
Sigmoid Function
</p>

In logistic reggression we do not use a squared error loss functions du to local optimum issues in the optimization model.
Instead we use L(yhat,y) = -(ylog(yhat) + (1-y)log(1-yhat)).

Gradient descent takes steps in the steepest direction iteratively to find the global optimum on the convex space of the cost function using w and b. J(w,b).
In gradient descent alpha is the learning rate of the algorithm.

You only need an intuitive understanding of calculus and derivatives to apply deep learning techniques, so the course spent some time reviewing these subjects.
Derivatives are the slope of a function at any given point on the function. The slope is not necessarily constant across the function.

#### Python and Vectorization

Vectorization is removing explicit for loops in code. Working with large datasets can be very slow and vectorization can improve processing times.
Whenever possible, avoid using explicit for loops.
Here is an article describing the example shown in the course: https://www.geeksforgeeks.org/vectorization-in-python/

The term broadcasting describes how numpy treats arrays with different shapes during arithmetic operations.
Subject to certain constraints, the smaller array is “broadcast” across the larger array so that they have compatible shapes.
Broadcasting provides a means of vectorizing array operations so that looping occurs in C instead of Python.
It does this without making needless copies of data and usually leads to efficient algorithm implementations.
Article describing broadcasting: https://numpy.org/doc/stable/user/basics.broadcasting.html

<p align="center">
<img src="https://github.com/peterhall71/coursera_Neural_Networks_and_Deep_Learning/blob/master/images/BroadcastingExample.jpg"  alt="Broadcasting Example" width="400"/>
</p>
<p align="center">
Broadcasting Example
</p>

### Week 3

#### Shallow Neural Networks

The neural network is made up of an input layer, a hidden layer, and an output layer.
The hidden layer is called this because it is not seen in the training set. This is called a two layer neural network, you do not count the input layer.
Each node in the hidden layer has two parameters (w,b). The output layer also has two parameters (w,b).
Article describing the structure of artificial neural networks: https://becominghuman.ai/understanding-the-structure-of-neural-networks-1fa5bd17fef0

<p align="center">
<img src="https://github.com/peterhall71/coursera_Neural_Networks_and_Deep_Learning/blob/master/images/neural_network_structure.PNG"  alt="Neural Network Structure" width="400"/>
</p>
<p align="center">
Neural Network Structure
</p>

Up until now we have been using the sigmoid activation function in the hidden layers.
Hyperbolic tangent function almost always works better than sigmoid.
Similar to centering data on the mean of the sample, having the mean of the function as zero makes learning for the next layer easier.
The exception is the output layer, since the output is between zero and one.

One downside in both sigmoid and tanh function is if z is very larger or small the slope of the function is close to zero.
ReLU function is used in these cases since the slope is zero when z is negative and one when z is positive.

<p align="center">
<img src="https://github.com/peterhall71/coursera_Neural_Networks_and_Deep_Learning/blob/master/images/activation_functions.png"  alt="Activation Functions" width="600"/>
</p>
<p align="center">
Activation Functions
</p>

