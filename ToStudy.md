## Optimization algorithms
    - Why is the best mini-batch size usually not 1 and not m, but instead something in-between?
    - Adam
    - Momentum
    
    출처 http://shuuki4.github.io/deep%20learning/2016/05/20/Gradient-Descent-Algorithm-Overview.html
    
## Bird recognition in the city of Peacetopia
    - What's difference human-level perormance and Bayes error
    - What happens after decrease the regularization
    - You have more false negatives than other's algorithm, What will you do?
    ----------------------------------------------------------------
    > Rethink the appropriate metric for this task, and ask your team to tune to the new metric.
    
    - You have only 1,000 images of the new species of bird. The city expects a better system from you within the next 3 months. Which of these should you do first?
    ----------------------------------------------------------------
    > Use the data you have to define a new evaluation metric (using a new dev/test set) taking into account the new species, and use that to drive further progress for your team.
    
## Autonomous driving ( case study )
    - Transfer Learning ?
    ----------------------------------------------------------------
    > 
    
    - Multi-task Learning ?
    ----------------------------------------------------------------
    > Red, Green signal -> OneHot -> [ 1, 0]
    
    - trainsing-dev, dev, test, what is difference ?
    
    - What is "swamping"?
    > Swamping and Masking Problem
    > Swamping : 정상치가 이상치에 가까운 경우 이상치로 잘못 분류하게 되는 현상
    > Masking : 이상치가 군집화되어 있으면 정상치로 잘못 분류하게 되는 현상.
    
    - end to end approach, step by step approach