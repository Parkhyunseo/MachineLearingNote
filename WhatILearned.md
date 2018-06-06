### Structuring Machine Learning
* Adding this data to the training set will change the training set distribution. However, it is not a problem to have different training and dev distribution. On the contrary, it would be very problematic to have different dev and test set distributions.
* A learning algorithm’s performance can be better than human-level performance but it can never be better than Bayes error.
* Softmax would be a good choice if one and only one of the possibilities (stop sign, speed bump, pedestrian crossing, green light and red light) was present in each image.
* Focus on images that the algorithm got wrong. Also, 500 is enough to give you a good initial sense of the error statistics. There’s probably no need to look at 10,000, which will take a long time.
* As seen in the lecture on multi-task learning, you can compute the cost such that it is not influenced by the fact that some entries haven’t been labeled.


### The basics of ConvNets
* Let's thinking 1D, 2D convolutions exmaple
* Convolution's operation used to extract the appropriate feature using a filter or kernel
* CNN is the key to automatically creating the kernel!
* When doing machine learning with image data, Normal NN is inefficient.
*   More the number of parameters, More overfitting.
* What is different ConvNet with Normal NN?
    ConvNet architecture can encode characteristics of image data because of the assumption that input data is an image. This architecture allows for more effective implementation of forward functions and greatly reduces the number of parameters required to learn the network.
* Structured
    Convolutional Layer, Pooling Layer, Fully-connected Layer
    Some layers have parameters and others or not
    Some layers have hyperparameter and others or not
* Local connectivity
    레이어의 각 뉴런을 입력 볼륨의 로컬 영역(receptive field)에만 연결
    볼륨의 깊이는 입력 볼륨의 깊이를 따른다.
* (W-F+2P)/S + 1, 출력 볼륨의 공간적 크기 X Y 
* Share Parameter
    ConvNet의 Parameter 개수를 조절하기 위해 사용된다.
    depth slice
    Layer의 가중치는 Fiter또는 Kernel이라고 부른다.
    Convolution의 결과물은 Activation map이 되며 각 깊이에 해당하는 필터의 액티베이션 맵들을 쌓으면 최종 출력 볼륨이 된다.
* Filter
* Padding
* Stride
* Pooling
* 'same' option
* "sparsity of connections"
* 공부자료 http://taewan.kim/post/cnn/
* Convolution functions, including
    - Zero Padding
    - Convolve window
    - Convolution forward
    - Convolution backward (optional)
* Pooling functions, including:
    - Pooling forward
    - Create mask
    - Distribute value
    - Pooling backward (optional)
