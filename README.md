## Practical aspects of deep learning 

### 1. If you have 10,000,000 examples, how would you split the train/dev/test set?
    * 98 % train, 1% dev, 1% test     

### 2. The dev and test set should :
    * Come from the same distribution

### 3. If your Neural Network model seems to have high bias, what of the following would be promising things to try?
    * Increase the number of units in each hidden layer [O]
    * Make the Neural Network deeper [O]
    * Add regularization
    * Get more test data 
    * Get more training data
    
### 4. You are working on an automated check-out kiosk for a supermarket, and are building a classifier for apples, bananas and oranges. Suppose your classifier obtains a training set error of 0.5%, and a dev set error of 7%. Which of the following are promising things to try to improve your classifier?
    * Increasing the regularization paramter lambda
    * Get more training data

### 5. What is weight decay?
    * A regularization technique (such as L2 regularization) that results in gradient descent shrinking the weights on every iteration.

### 6. What happens when you increase the regularization hyperparameter lambda?
    * Weights are pushed toward becoming smaller (closer to 0)

### 7. With the inverted dropout technique, at test time:
    * You do not apply dropout (do not randomly eliminate units) and do not keep the 1/keep_prob factor in the calculations used in training

### 8. Increasing the parameter keep_prob from (say) 0.5 to 0.6 will likely cause the following:
    * Increasing the regularization effect
    * Reducing the regularization effect [O] ???
    * Causing the neural network to end up with a higher training set error
    * Causing the neural network to end up with a lower training set error [O]

### 9. Which of these techniques are useful for reducing variance (reducing overftting) ?
    * Data augmentation
    * Dropout
    * L2 regularization
    
### 10. Why do we normalize the inputs xx?
    * It makes the cost function faster to optimize