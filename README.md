# Introduction
This repository serves as an introduction to some of the basic activation functions used in neural networks.
Example used will be the network architecture found in the neural_network_from scratch repository.

# Partial derivatives from example
dSSR/db1[Using chain rule] = dSSR/dPredicted * dPredicted/dy1 * dy1/dx1 * dx1/db1 \
dSSR/db2[Using chain rule] = dSSR/dPredicted * dPredicted/dy2 * dy2/dx2 * dx2/db2 \
dSSR/dw1[Using chain rule] = dSSR/dPredicted * dPredicted/dy1 * dy1/dx1 * dx1/dw1 \
dSSR/dw2[Using chain rule] = dSSR/dPredicted * dPredicted/dy2 * dy2/dx2 * dx2/dw2 

# Sigmoid
![alt text](https://github.com/kwquan/activation_functions/blob/main/sigmoid.jpeg)

The sigmoid function squeezes values in between 0 & 1, with the y-intercept at 0.5

![alt text](https://github.com/kwquan/activation_functions/blob/main/sigmoid-derivative.jpeg)

1 issue with the sigmoid activation function is it's low derivative values. \
Notice how the derivative values approach 0 especially for x-values > 3 or < -3. \
As observed from the derivative graph above, the highest derivative is only 0.25, occuring at x=0. \
This makes it very susceptible to the vanishing gradient problem where increasing products of small derivative values will produce almost-zero step sizes. \
Equation for derivative is: sigmoid(x)(1-sigmoid(x))

# TanH
![alt text](https://github.com/kwquan/activation_functions/blob/main/tanh.png)

The hyperbolic-tangent activation function squeezes values between -1 & 1, with y-intercept=0 when x=0

![alt text](https://github.com/kwquan/activation_functions/blob/main/tanh-derivative.png)

Unlike the sigmoid function, the tanh function mitigates the issue of vanishing gradient by allowing for larger derivative values especially for x-values close to 0. \
However, it is still susceptible to vanishing gradient issue for very-positive/very-negative x-values. \
Maximum derivative is 1 when x=0 \
Equation for derivative is: 1-tanh^2(x)

# Relu
![alt text](https://github.com/kwquan/activation_functions/blob/main/relu.png)

The rectified linear unit is a simple activation function that is linear for x>=0 values & 0 for x<0 values

![alt text](https://github.com/kwquan/activation_functions/blob/main/relu-derivative.png)

Unlike the above 2 functions, the relu function solves the issue of vanishing gradient by fixing the derivative value at 1 for positive x values. \
This ensures that multiple products will not lead to ever-decreasing step-sizes. \
However, the design of fixing derivative value as 0 for negative x values creates the issue of dead neurons since those neurons will never be updated as long as x values are negative. \
Derivative value=1 for x>=0 else 0 \
Derivative is: 1 for x>=0 else 0
