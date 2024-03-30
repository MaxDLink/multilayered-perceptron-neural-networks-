## How to Run 

1. Clone this repo
2. Open the .ipynb file in either visual studio code's jupyter notebook extension environment or jupyter notebook
3. Select a python environment with the appropriate packages installed for the project 


## Project Overview 

This project takes child poverty data & organizes it by classes. The classes are low poverty, medium poverty, high poverty, & extreme poverty. 

The poverty classes are the target (y) that the neural network model tries to predict with input data (X). The training data is split 80% training & 20% testing. 

 A two layer perceptron class is created as a base class & a bunch of subclasses are created to try different methods for adjusting the model’s neuron weights etc. In addition to this, more networks are made with 3, 4, & 5 layers. Adding more layers to a network lets it interpret more advanced information, at the cost of reducing noise, so the amount of layers you want depends on the type of data. The accuracy mean scores of these different networks are all compared against each other. 


The weights are adjusted with gradient descent methods, the learning rate (eta) is adjusted, and momentum is applied etc.

The RMSProp & AdaM are two special additions to the neural network. RMSProp remembers past learning rates (etas) so that the learning rates can be adjusted smoother. AdaM remembers past learning rates & also remembers past momentum of the gradients, so that the model doesn’t get stuck in local minima. 

It’s like pushing a ball down a hill, you want the ball to go down the hill as far as it can, but sometimes the ball gets stuck in a valley. If you give the ball extra momentum, by adding a little of your past momentum, then the ball may make it over the valley dip & actually roll down the hill even further.

The different model techniques (RMSProp, AdaM, & the standards with different layer amounts) all have different accuracy means, and the accuracy means are checked with the confidence interval. The confidence interval compares two models. If the confidence interval has a negative lower bound & a positive upper bound, then the range includes 0, which means that the actual difference between these two models mean scores could be 0…. But if the confidence interval’s lower bound & upper bound never include 0 then the mean score difference in the two models may actually exist. You need a confidence interval check because any mean score differences could be from random variation in data, so there could not be any significant difference in mean scores in reality. 

On each gradient average graph, you can see how the weights swing significantly at first on each layer of the networks, but as the gradient converges closer to zero, the weights swing less as the model doesn’t have as much to learn. Pretty interesting stuff!

## Packages needed for this project.... 

