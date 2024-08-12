

# AutoDiff Package

## Overview

The **AutoDiff** package is a Python library that provides functions for automatic differentiation and neural network training. It includes modules for defining variables, biases, linear layers, activation functions, loss functions, and training utilities.

## How to Run the Code

1. Clone the repository to your local machine.
2. Navigate to the repository directory.
3. Run the `main.py` file.

You can adjust the number of epochs, batch size, and learning rate at the beginning of the `main.py` file to modify the training parameters.

## Test Code

When running `main.py`, the following steps are performed:

1. Load the training data using the `dataloader()` function from a provided pickle file.
2. Train the neural network using the `train()` function.
3. Display the results, including losses and optional gradients.

## Package Code

### Functions and Classes

1. **Variable Class**: The basic building block that contains data and gradients.
   - `forward()`: Returns the stored data value and initiates the forward pass.
   - `backward(value, learning_rate)`: Computes gradients and updates the variable.

2. **MatrixMul Class**: Computes matrix multiplication.
   - `forward(matrixA, matrixB)`: Multiplies two matrices.
   - `backward(value, learning_rate)`: Computes gradients and updates the inputs.

3. **ReLU Class**: Implements the ReLU activation function.
   - `forward(prevOperation)`: Applies the ReLU activation.
   - `backward(value, learning_rate)`: Computes gradients.

4. **RegressionLoss Class**: Computes the mean squared error for regression tasks.
   - `forward(original, predicted)`: Calculates the MSE loss.
   - `backward(value, learning_rate)`: Computes gradients.

5. **BinaryLoss Class**: Computes binary cross-entropy loss for binary classification tasks.
   - `forward(original, predicted)`: Calculates the binary cross-entropy loss.
   - `backward(value, learning_rate)`: Computes gradients.

6. **Add Class**: Performs element-wise addition of two matrices.
   - `forward(f_input1, f_input2)`: Adds two input matrices.
   - `backward(b_grad, learning_rate)`: Computes gradients.

7. **Bias Class**: Represents bias terms in neural networks.
   - Custom `backward()` method to update bias values.

8. **Linear Class**: Represents a fully connected layer in a neural network.
   - `forward(x)`: Computes the forward pass for the layer.
   - `backward(grad, learning_rate)`: Computes gradients and propagates them back.
