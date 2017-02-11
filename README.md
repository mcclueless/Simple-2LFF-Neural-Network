# Simple-2-Layer-Neural-Network

There are certain better introduction to a perceptron and Neural Networks in general and I stick here largely to my own wording for the purpose of understanding. 

Really good instructions are a lot out there. I like in particular this one:

http://stevenmiller888.github.io/mind-how-to-build-a-neural-network/

Good resources to get started with Deep Learning and Neural Network are:

Glossary of terms: https://docs.google.com/document/d/1Vy6IN-LuttLtA7Wzb2WduL8jcU1AuF3-Oygu8prp2m4/edit?usp=sharing

Currated list or resources: https://docs.google.com/spreadsheets/d/1NZtIxDWiJ_B0UKhIDUk-wTZAT3Fxfh-fGwcQKXg1bQU/edit?usp=sharing


A pretty example of how a perceptron works is available here: http://maerch.github.io/static/vpercp/
It gives a clear overview how it makes a "line of best fit" that makes the prediction. Ultimately, a perceptron is a statistical model that once trained can be sampled to retrieve predictions.


Here are some:

Introduction to Deep Learning with Siraj: https://www.youtube.com/watch?v=vOppzHpvTiQ
Demo of using linear regression: https://github.com/amanullahtariq/MLAlgorithm/tree/eca367287f7874e08a790ce0b0c21567e0b38a22/Challenge/LinearRegression
A quiet different kind of learning technique: https://www.youtube.com/watch?v=1L0TKZQcUtA

A one layer feed forward Neural Network example in python is here: https://github.com/stmorgan/pythonNNexample

A Neural Network is a biologically inspired algorythm that learns to idenfity pattern in data. The simplest one is called a perceptron. A perceptron is also called a single layer feed forward neural network. The reason it is called single layer is because it only has and feed forward because data is only flowing into one direction.

These algorithms essentially apply a series of computations to matrices. In practice the Neural Network makes predictions that largely depend on the weights. Adjusting this weights is done by calculating and updating these with the error in accordance to the change of that error. 

That's how it looks like a bit more mathematically

<img src="https://github.com/mcclueless/Simple-2LFF-Neural-Network/blob/master/assets/perceptron.png" width="400">

In this example the network has two layers, a hidden layer and an output layer. The hidden layer will use the sigmoid function for activations. The output layer has only one node and is used for the regression, the output of the node is the same as the input of the node. As a method of propagating the error back to adjust the weights we use gradient descent. Its a method that calculates the error and uses that value to update the weights of the input to slowly find the "line of best fit".


The way this example looks like is this:

Basic Look:
 <img src="https://raw.githubusercontent.com/mcclueless/Simple-2LFF-Neural-Network/master/assets/network-with-labeled-nodes.png?raw=true" width="400"/>

The main difference between a simple perceptron (single layer feed forward neural network) and a two layer version is that the weights are now matrices and backpropagation is uses. Just as we want to send the input from the output of the first layer forward to the input of the hidden one (forward propagation) we also want to propagate the error of the output of the output layer all the way back. This is called backward propagation. On easy way to imagine it is to flip the network upside down.

More info on the concept of Backpropagation: http://neuralnetworksanddeeplearning.com/chap2.html

So what happens here in the code is that the is that the algorythm is initiated which means that its weights are randomized and its activation function turned on. When we start to train the network there are hyperparameters at work:

1. Number of epochs
Its the number of times the dataset passes through the network.

2. Learning rate
Scales the step size of the rate of change (of the error) with which the weights are updated.

3. Hidden nodes
Sets the number of hidden nodes the network can utilize to improve its predictions. 


The rest is well described in the ipython notebook. have fun!




