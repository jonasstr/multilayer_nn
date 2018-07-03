# Experimental NN-library for Python 3

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

To evaluate the accuracy of the model on the test set, use the NeuralNetwork.predict() function.
This function requires a single element from the test set and returns the predicted output for this element.

Example:
```python
pred = nn.predict(test_X[i])
```