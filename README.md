# Neural Networks and Deep Learning  
### deeplearning.ai  
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
Instead we use L(yhat,y) = -ylog(yhat) + (1-y)log(1-yhat).

Gradient descent takes steps in the steepest direction iteratively to find the global optimum on the convex space of the cost function using w and b. J(w,b).
In gradient descent alpha is the learning rate of the algorithm.

You only need an intuitive understanding of calculus and derivatives to apply deep learning techniques, so the course spent some time reviewing these subjects.
Derivatives are the slope of a function at any given point on the function. The slope is not necessarily constant across the function.

#### Python and Vectorization

