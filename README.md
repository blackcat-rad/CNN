# A complete CNN model from  scratch using PyTorch

### Want to train a 10 class classification dataset (STL-10) from complete scratch. It is only for intuition purpose, so the accuracy might be not ideal. Here we want to ensure to use libraries as low as possible

## Training Overview
##Training a neural network typically consists of two phases:

- A forward phase, where the input is passed completely through the network.
- A backward phase, where gradients are backpropagated (backprop) and weights are updated.
### We’ll follow this pattern to train our CNN. There are also two major implementation-specific ideas we’ll use:

### During the forward phase, each layer will cache any data (like inputs, intermediate values, etc) it’ll need for the backward phase. This means that any backward phase must be preceded by a corresponding forward phase.
### During the backward phase, each layer will receive a gradient and also return a gradient. It will receive the gradient of loss with respect to its outputs ∂out/∂L and return the gradient of loss with respect to its inputs ∂in/∂L

### We have to calculate the derivative of the loss with respect of weight and biases. We have to backpropagate the loss where we can calculate it. L=-summation(Yi log(yi)).Which is cross entropy loss. where i=1 from c where c is class. Logits are transforming using probability. 

### yi=e^zi/summation(e^zk)
### zl=summation(wjlxj) which is softmax transfar
