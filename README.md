# Recognize-Handwritten-Notes
# Step 1 — Configuring the Project
Before you can develop the recognition program, you’ll need to install a few dependencies and create a workspace to hold your files.
We’ll use a Python 3 virtual environment to manage our project’s dependencies. Create a new directory for your project and navigate to thenew directory

# Step 2 — Importing the MNIST Dataset
The dataset we will be using in this tutorial is called the MNIST dataset,and it is a classic in the machine learning community. This dataset is 
made up of images of handwritten digits, 28x28 pixels in size. Here are some examples of the digits included in the dataset:
![image](https://user-images.githubusercontent.com/70911721/186297711-dbe003a8-38b4-4cc3-b379-211c41b69f7a.png)

# Step 3 — Defining the Neural Network Architecture
The architecture of the neural network refers to elements such as the number of layers in the network, the number of units in each layer, and how the units are connected between layers. As neural networks are loosely inspired by the workings of the human brain, here the term unit is used to represent what we would biologically think of as a neuron. Like neurons passing signals around the brain, units take some values from previous units as input, perform a computation, and then pass on the new value as output to other units. These units are layered to form the network, starting at a minimum with one layer for inputting values, and one layer to output values. The term hidden layer is used for all of the layers in between the input and output layers, i.e. those “hidden” from the real world.Different architectures can yield dramatically different results, as the performance can be thought of as a function of the architecture among other things, such as the parameters, the data, and the duration of training. Add the following lines of code to your file to store the number of units per layer in global variables. This allows us to alter the network architecture in one place, and at the end of the tutorial you can test for yourself how different numbers of layers and units will impact the results of our model.
![image](https://user-images.githubusercontent.com/70911721/186299903-d7e11655-95bf-461c-9713-9652ec2cb7f8.png)


# Step 4 — Building the TensorFlow Graph
To build our network, we will set up the network as a computational graph for TensorFlow to execute. The core concept of TensorFlow is the tensor, a data structure similar to an array or list. initialized, manipulated as they are passed through the graph, and updated through the learning process.

# Step 5 — Training and Testing
The training process involves feeding the training dataset through the graph and optimizing the loss function. Every time the network iterates through a batch of more training images, it updates the parameters to reduce the loss in order to more accurately predict the digits shown. The testing process involves running our testing dataset through the trained graph, and keeping track of the number of images that are correctly predicted, so that we can calculate the accuracy. Before starting the training process, we will define our method of evaluating the accuracy so we can print it out on mini-batches of data while we train. These printed statements will allow us to check that from the first iteration to the last, loss decreases and accuracy increases; they will also allow us to track whether or not we have ran enough iterations to reach a consistent and optimal result.
# Conclusion
In this tutorial you successfully trained a neural network to classify the MNIST dataset with around 92% accuracy and tested it on an image ofyour own. Current state-of-the-art research achieves around 99% on this same problem, using more complex network architectures involving convolutional layers. These use the 2D structure of the image to better represent the contents, unlike our method which flattened all the pixels.
