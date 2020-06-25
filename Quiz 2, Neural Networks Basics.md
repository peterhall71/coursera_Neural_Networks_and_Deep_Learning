## Quiz 2: Neural Network Basics

#### Question 1: What does a neuron compute?
Answer:  
A neuron computes the mean of all the features before applying the output to an activation function.  

#### Question 2: Which of these is the "Logistic Loss"?  
Answer:  
L(yhat,y) = -(ylog(yhat) + (1-y)log(1-yhat))  

#### Question 3: Suppose img is a (32,32,3) array, representing a 32x32 image with 3 color channels red, green and blue. How do you reshape this into a column vector?
Answer:  
x = img.reshape((32\*32\*3,1))  

#### Question 4: Consider the two following random arrays "a" and "b". What will be the shape of "c"?
a = np.random.randn(2, 3) # a.shape = (2, 3)  
b = np.random.randn(2, 1) # b.shape = (2, 1)  
c = a + b  

Answer:  
c.shape = (2, 3)  

#### Question 5: Consider the two following random arrays "a" and "b". What will be the shape of "c"?
a = np.random.randn(4, 3) # a.shape = (4, 3)  
b = np.random.randn(3, 2) # b.shape = (3, 2)  
c = a\*b  

Answer:  
The computation cannot happen because the sizes dont match. It's going to be "Error"!  

#### Question 6: Suppose you have n_x​ input features per example. Recall that X=[x^(1)x^(2)...x^(m)]. What is the dimension of X? 
Answer:  
(n_x,m)  

#### Question 7: Recall that "np.dot(a,b)" performs a matrix multiplication on a and b, whereas "a*b" performs an element-wise multiplication. Consider the two following random arrays "a" and "b". What is the shape of c?
a = np.random.randn(12288, 150) # a.shape = (12288, 150)  
b = np.random.randn(150, 45) # b.shape = (150, 45)  
c = np.dot(a,b)  

Answer:  
c.shape = (12288, 45)  

#### Question 8: Consider the following code snippet. How do you vectorize this?

a.shape = (3,4)
b.shape = (4,1)

for i in range(3):
  for j in range(4):
    c[i][j] = a[i][j] + b[j]

Answer:  
c = a + b.T  

#### Question 9: Consider the following code. What will be c? (If you’re not sure, feel free to run this in python to find out).

a = np.random.randn(3, 3)  
b = np.random.randn(3, 1)  
c = a\*b  

Answer:  
This will invoke broadcasting, so b is copied three times to become (3,3), and \* is an element-wise product so c.shape = (3, 3)  


#### Question 10: Consider the following computation graph. What is the output J?

<p align="center">
<img src="https://github.com/peterhall71/coursera_Neural_Networks_and_Deep_Learning/blob/master/images/computation_graph.png" alt="Computation Graph" width="400"/>
</p>

Answer:  
(a - 1) \* (b + c)  