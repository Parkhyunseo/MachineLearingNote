* Tensorflow Tutorial, I how know how to
    1. Create placeholders
    2. Specify the computation graph corresponding to operations you want to compute
    3. Create the session
    4. Run the session, using a feed dictionary if necessary to specify placeholder variables' values
    

* Remember
    - Tensorflow is a programming framework used in deep learning
    - The two main object classes in tensorflow are Tensors and Operators.
    - When you code in tensorflow you have to take the following steps:
        Create a graph containing Tensors (Variables, Placeholders ...) and Operations (tf.matmul, tf.add, ...)
        Create a session
        Initialize the session
        Run the session to execute the graph
    - You can execute the graph multiple times as you've seen in model()
    - The backpropagation and optimization is automatically done when running the session on the "optimizer" object.