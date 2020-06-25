Question 1:	What does a neuron compute?
Answer: 	A neuron computes the mean of all the features before applying the output to an activation function.

Question 2: Which of these is the "Logistic Loss"?
Answer: 	L(yhat,y) = -(ylog(yhat) + (1-y)log(1-yhat))
		
Question 3: Suppose img is a (32,32,3) array, representing a 32x32 image with 3 color channels red, green and blue. How do you reshape this into a column vector?
Answer: 	x = img.reshape((32*32*3,1))

Question 4: Consider the two following random arrays "a" and "b". What will be the shape of "c"?
			a = np.random.randn(2, 3) # a.shape = (2, 3)
			b = np.random.randn(2, 1) # b.shape = (2, 1)
			c = a + b
Answer: 	c.shape = (2, 3)

Question 5: Consider the two following random arrays "a" and "b". What will be the shape of "c"?
Answer: 	The computation cannot happen because the sizes dont match. It's going to be "Error"!

Question 6: Images for cat recognition is an example of "structured" data, because it is represented as a structured 
			array in a computer. True/False?
Answer: 	False

Question 7: A demographic dataset with statistics on different cities' population, GDP per capita, economic growth, is an example of 
			"unstructured" data because it contains data coming from different sources. True/False?
Answer: 	False

Question 8: Why is an RNN used for machine translation, say translating English to French?
Answer: 	It can be trained as a supervised learning problem.
			It is applicable when the input/output is a sequence.
			RNNs represent the recurrent process of Idea->Code->Experiment->Idea->...

Question 9: In this diagram which we hand-drew in lecture, what do the horizontal axis and vertical axis represent?
Answer: 	x-axis is the amount of data.
			y-axis is the performance of the algorithm.

Question 10: Assuming the trends described in the previous question's figure are accurate, which of the following are true?
Answer: 	Increasing the size of a neural network generally does not hurt an algorithm's performance, and it may help significantly.
			Increasing the training set size generally does not hurt an algorithm's performance, and it may help significantly.