# Initializing all the weiths to zero results in the network failing to break symmetry.
    - This means that every neuron in each layer will learn the same thing.
    - you might as well be training a neural network with n[l] = 1 for every layer
    - the network is no more powerful than a linear classifier such as logistic regression.
    
    