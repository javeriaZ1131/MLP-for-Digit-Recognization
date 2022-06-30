# MLP-for-Digit-Recognization
 
 Apply the MLP for digit recognization and perform the complete analysis of this implementation in terms of  calculation accuracy,recall and percision.
 
 

 
 ----------------------------------------------------------Multi-Layer Perceptron----------------------------------------------------.

Multi layer perceptron also called MLP or simple Perceptron has a dense layer of neurons in it.  Each node perform following computation on each node which is denoted by the equation
N= Σwixi+b where x denotes the input to that neuron ,w is the weight and b is the bias value.initially two values are selected randomly and then these values keep on updated  as the NN learns in order to get  reach the optimize decision.in MLPs, the flow of data is only towards forward direction that is why they are also called as Feed Forward Networks.The algorithm essentially is trained on the data in order to learn a function. Given a set of features and a target variable (e.g. labels) it learns a nonlinear function for either classification or regression.The training data of  A x B pixel format  is converted in the form of an input vector.
There are 3 main layers
1-input layer 
2- hidden layers(Minimum 1 or can be more than 1 hidden layers)  
3- output layer

Multi-layer perceptron for digit Recognition :

Step by step MNIST digit recognition using  Multi Layer perceptron:

Step 1: 
Firstly we will load the mnist data containing digits from 0-9 and perform the splitting and training and testing of the dataset(build in dataset mnist dataset). Mnist dataset consists of  handwritten digits in different styles.There are 10,000 input data elements and each of 28 x 28 pixels.
 

The MNIST dataset contains only grayscale images.
Step 2:
The sample of pixel distribution graph for the single digit from the mnist dataset.

Step 3: 
In order to train our neural network in multi layer perceptron  we have to firstly  classify images. We first have to unroll the height x width pixel format into one big vector - the input vector. 

So its length in our case be 28* 28 = 784. Here the data is also normalized the data too.

After conversion to vector we get the total input data of 10000 each of length 784. This data will be then actually used in MLP for processing.
 

Step 4:
Now we have to create the MLP . where the 3 components of input 2 hidden layers and a output layer is implemented .
Input layer is  784 pixel input vector        relu function is used 
2 hidden layer each of 600 nodes        relu function  is used 
Output layer of 10 categories(0-9)    sigmoid function used at Output layer.

Step 5:
Now we  have to start the training process where the model will start the processing to make predictions. We need to  specify how many times we want to iterate on the whole training set (epochs) and how many samples we use for one update to the model's weights (batch size). It is an effective approach to take the bigger batch, because the  stochastic gradient descent updates will be more stable . But due to  PC restrictions  batch size of 128 and 10 interations(epochs) are taken . 
The Output show the accuracy on each iterations

On seeing the training process we can observe that as the iterations are proegressig the accruacy if the training data also increases as compared to the test data.

Step 6:
Calculate the accuracy of the model perform to check how well and accurate the model is making the predictions . The model.evaluate() method computes the loss and any metric defined when compiling the model. 
 
On evaluating the accuracy we get the accuracy of 0.9804.
Step 7:
Generate predictions  which was made by model and check  how many predictions done by model correctly and incorrectly.
On taking 600 nodes in each hidden layer we can see that the from the sample of 10,000 9805 numbers are predicted by MLP with 2 hidden layers correctly while only 195 are predicted by model incorrectly. The example of incorrect predictions is in(Fig-2).
  
Step 8:
Now  the precision is calculated. For that the classification.report() function is used.
The precision calculated is 0.98% (98%).
The recall calculated is 0.98%(98%)
The accuracy calculated is 0.98%(98%).

Conclusion:

The accuracy and precision can be further improved by either increasing the number of hidden layers(sometimes not it depends on the complexity of problem) or increasing the number of nodes on each layer.








Conclusion:

The accuracy and precision can be further improved by either increasing the number of hidden layers(sometimes not it depends on the complexity of problem) or increasing the number of nodes on each layer.

