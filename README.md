# Multi-Bit XOR Perceptron

## Overview

This project implements a perceptron model to perform the XOR operation on multi-bit binary numbers. The primary function is designed to take two binary inputs of equal length and compute their bitwise XOR using a simple neural network model.

## Code Explanation

The implementation consists of several functions:

- **unitStep(v)**: A basic activation function that returns 1 if `v` is greater than or equal to 0; otherwise, it returns 0.

- **perceptronModel(x, w, b)**: A function that calculates the output of a perceptron model based on the input vector `x`, weights `w`, and bias `b`.

- **NOT_logicFunction(x)**: Returns the NOT of the input using a perceptron.

- **AND_logicFunction(x)**: Returns the AND of the input using a perceptron.

- **OR_logicFunction(x)**: Returns the OR of the input using a perceptron.

- **XOR_logicFunction(x)**: Computes XOR for two binary inputs using AND, OR, and NOT functions.

- **multiBitXOR(a, b)**: This function takes two binary arrays of equal length, computes the XOR for each corresponding bit using the `XOR_logicFunction`, and returns the result as an array.

## Example Usage

The following code demonstrates how to use the implemented functions to compute the XOR of two multi-bit binary numbers:

```python
import numpy as np

# 3-bit binary numbers
a = np.array([1, 0, 1])  # Binary for 5
b = np.array([0, 1, 1])  # Binary for 3

# 4-bit binary numbers
c = np.array([1, 0, 1, 0])  # Binary for 10
d = np.array([1, 1, 0, 1])  # Binary for 13

print("XOR of {} and {} = {}".format(a, b, multiBitXOR(a, b)))
print("XOR of {} and {} = {}".format(c, d, multiBitXOR(c, d)))

```

## Output 

```python
XOR of [1 0 1] and [0 1 1] = [1. 1. 0.]
XOR of [1 0 1 0] and [1 1 0 1] = [0. 1. 1. 1.]

```




