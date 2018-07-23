# Experimental NN-library for Python 3

If you are unable to view the notebook use the following link:  
https://nbviewer.jupyter.org/github/jonasstr/multilayer_nn/blob/master/Neural%20Network%20v3.ipynb

## Usage
Use the constructor of the NeuralNetwork class to create a new network.
You must specify the number of input neurons, a list containing the number of neurons for a variable amount of hidden layers, the number of output neurons, the learning rate, as well as the activation function.

Example:
```python
nn = NeuralNetwork(4, [2,3], 3, lr=0.01, activation='sigmoid')
```

Use the NeuralNetwork.train() function to train the network.
The function takes the inputs and target lists as parameters, an optional bool parameter to specify whether to convert the input list into a onehot-list, the number of iterations to train the network (epochs), as well a display_step parameter for visualization.

Example:
```python
nn.train(train_X, train_y, convert=True, epochs=200, display_step=20)
```

To evaluate the accuracy of the model on the dataset, use the NeuralNetwork.accuracy() function. This function requires the inputs and targets of the respective dataset.

Example:
```python
acc = nn.accuracy(test_X, test_y)
```

You can also use NeuralNetwork.predict() to get the predicted value for one element of the test set. A return value of zero means the first neuron in the output layer has been activated.

Example:
```python
pred = nn.predict(test_X[i])
```
