# Neural Network Backpropagation Explanation

This document explains the backpropagation process in a neural network through a series of mathematical expressions. We'll break down the process step by step.

## Introduction
Backpropagation is a fundamental concept in training neural networks. It involves calculating gradients of the loss function with respect to the weights of the network, allowing us to update the weights and minimize the error during training.

## Formulas

### Definitions
- `h1`, `h2`: Hidden layer neuron inputs
- `a_h1`, `a_h2`: Activation of hidden layer neurons
- `o1`, `o2`: Output layer neuron inputs
- `a_o1`, `a_o2`: Activation of output layer neurons
- `E_total`: Total error
- `E1`, `E2`: Individual errors for each output neuron
- `t1`, `t2`: Target outputs
- `w`: Weights

### Key Equations
- `∂E_total/∂w`: Gradient of the total error with respect to a weight
- `∂E_total/∂a_h`: Gradient of the total error with respect to the activation of hidden layer neurons

## Explanation
The document goes through the process of computing the gradient of the total error with respect to each weight in the network. It begins by expanding the expression for `∂E_total/∂w` using chain rule and then computing each component step by step.

### Weight Updates
- `∂E_total/∂w5`, `∂E_total/∂w6`, `∂E_total/∂w7`, `∂E_total/∂w8`: Gradients of the total error with respect to weights connecting the hidden and output layers.
- `∂E_total/∂w1`, `∂E_total/∂w2`, `∂E_total/∂w3`, `∂E_total/∂w4`: Gradients of the total error with respect to weights connecting the input and hidden layers.
