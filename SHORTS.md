# Initializing all the weiths to zero results in the network failing to break symmetry.
    - This means that every neuron in each layer will learn the same thing.
    - you might as well be training a neural network with n[l] = 1 for every layer
    - the network is no more powerful than a linear classifier such as logistic regression.
    
# What you should remember
    * The weights  W[l]W[l]  should be initialized randomly to break symmetry. It is however okay to initialize the biases  b[l]b[l]  to zeros. Symmetry is still broken so long as  W[l]W[l]  is initialized randomly.
    * Different initializations lead to different results
    * Random initialization is used to break symmetry and make sure different hidden units can learn different things
    * Don't intialize to values that are too large
    * He initialization works well for networks with ReLU activations.
    * Regularization will help you reduce overfitting.
    * Regularization will drive your weights to lower values.
    * L2 regularization and Dropout are two very effective regularization techniques.

# What you should remember - the implicatios of L2-regularization on:
    * The cost computation:
        - A regularization term is added to the cost
    * The backpropagation function:
        - There are extra terms in the gradients with respect to weight matrices
    * Weights end up smaller ("weight decay"):
        - Weights are pushed to smaller values.

# What you should remember about dropout:
    * What you should remember about dropout:
        - Dropout is a regularization technique.
    * You only use dropout during training. Don't use dropout (randomly eliminate nodes) during test time.
        - Apply dropout both during forward and backward propagation.
    * During training time, divide each dropout layer by keep_prob to keep the same expected value for the activations. For example, if keep_prob is 0.5, then we will on average shut down half the nodes, so the output will be scaled by 0.5 since only the remaining half are contributing to the solution. Dividing by 0.5 is equivalent to multiplying by 2. Hence, the output now has the same expected value. You can check that this works even when keep_prob is other values than 0.5.