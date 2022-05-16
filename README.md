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

1 issue with the sigmoid activation function is it's low derivative values. 
As observed from the derivative graph above, the highest derivative is only 0.25, occuring at x=0.
This makes it very susceptible to the vanishing gradient problem where increasing products of small derivative values will produce almost-zero step sizes.
