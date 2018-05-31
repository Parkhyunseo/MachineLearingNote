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
    * Gradient checking verifies closeness between the gradients from backpropagation and the numerical approximation of the gradient (computed using forward propagation).
    * Gradient checking is slow, so we don't run it in every iteration of training. You would usually run it only to make sure your code is correct, then turn it off and use backprop for the actual learning process.
    * The difference between gradient descent, mini-batch gradient descent and stochastic gradient descent is the number of examples you use to perform one update step.
    * You have to tune a learning rate hyperparameter  αα .
    * With a well-turned mini-batch size, usually it outperforms either gradient descent or stochastic gradient descent (particularly when the training set is large).
    * Momentum takes past gradients into account to smooth out the steps of gradient descent. It can be applied with batch gradient descent, mini-batch gradient descent or stochastic gradient descent.
    * You have to tune a momentum hyperparameter  ββ  and a learning rate  αα .

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

# Stochastic Gradient Descent (SGD) VS Gradient Descent (GD)
    SGD - It iteratively update only one sample in trainsing set.
    GD - It iteratively update whole sample
    
    * if training sample was big, GD was so slowly move.
    
# Optimization algorithms
    Momentum usually helps, but given the small learning rate and the simplistic dataset, its impact is almost negligeable. Also, the huge oscillations you see in the cost come from the fact that some minibatches are more difficult thans others for the optimization algorithm.
    Adam on the other hand, clearly outperforms mini-batch gradient descent and Momentum. If you run the model for more epochs on this simple dataset, all three methods will lead to very good results. However, you've seen that Adam converges a lot faster.

# Hyperparameter tuning, Batch Normalization
    - If searching among a large number of hyperparameters, you should try values in a random values.
    - Try random values, don't do grid search. Beacause you don't know which hyperparameters are more important than others.
    - some hyperparameters, such as the learning rate, are more critical than others.
    - Minor changes in your model could potentially need you to find good hyperparameters again from scratch.
    
# Bird recognition in the city of Peacetopia
    - What is the evaluation metric?
    - How do you structure your data into train/dev/test sets?
    
    - 요구사항이 있을 때 ex) 새로운 것을 학습하는데 n초 제한, 메모리 제한 등이 있을 때 제한되는 사항을 만족하는 상황에서 나머지 조건을 Optimization 시킨다.
    