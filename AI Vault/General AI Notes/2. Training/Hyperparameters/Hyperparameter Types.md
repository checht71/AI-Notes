  
Hyperparameters are external configuration settings that control various aspects of the training and architecture of a machine learning or deep learning model. These settings are set before the training process begins and are not learned from the data.

1. **[[Learning Rate Optimization]]**:
    - The learning rate determines the step size at which the model's parameters are updated during training. It controls how quickly or slowly the model learns from the data. A higher learning rate may lead to faster convergence but may also result in overshooting the optimal solution.
2. **Number of Epochs**:
    - The number of epochs specifies how many times the entire training dataset is passed forward and backward through the model. It affects how long the training process continues. Too few epochs may result in underfitting, while too many epochs can lead to overfitting.
3. **[[Batch Sizes]]**:
    - Batch size determines the number of data samples processed together in each training iteration. It impacts memory usage and training speed. Larger batch sizes can speed up training but may require more memory.
4. **Number of Layers and Units (Neurons)**:
    - The architecture of a neural network, including the number of layers and the number of units (neurons) in each layer, is a critical hyperparameter. It determines the model's capacity to learn complex patterns from data.
5. **[[Activation Functions]]**:
    - The choice of activation functions (e.g., ReLU, Sigmoid, Tanh) for the neurons in a neural network is a hyperparameter. Different activation functions introduce different levels of non-linearity to the model.
6. **[[Regularization]] Strength**:
    - Regularization hyperparameters, such as L1 and L2 regularization, control the penalty applied to the model's parameters to prevent overfitting. The strength of regularization is a hyperparameter.
7. **[[Dropout]] Rate**:
    - Dropout is a regularization technique where a fraction of neurons is randomly dropped out during training to prevent overfitting. The dropout rate specifies the fraction of neurons to drop in each layer and is a hyperparameter.
8. **[Optimizer Algorithm](Optimizers.md)**:
    - The choice of optimization algorithm (e.g., Adam, SGD, RMSprop) used to update the model's parameters is a hyperparameter. Different optimizers have different convergence behaviors.
9. **Initial Weights and Biases**:
    - The initial values of weights and biases in the model can affect training outcomes. Initializing them correctly is crucial. Hyperparameters related to weight initialization include weight initialization method and scale.
10. **Learning Rate Schedule**:
    - Learning rate schedules adjust the learning rate during training. For example, a learning rate may start high and gradually decrease. The schedule type and parameters are hyperparameters.
11. **Convolutional Kernel Size and Stride**:
    - In convolutional neural networks (CNNs), hyperparameters include the size and stride of convolutional kernels, which affect the spatial resolution of feature maps.
12. **[[Recurrent Neural Network]] (RNN) Hyperparameters**:
    - For RNNs, hyperparameters include the type of RNN cell (e.g., LSTM, GRU), the number of recurrent units, and the sequence length.
13. **Gradient Clipping**:
    - Gradient clipping is a technique to prevent exploding gradients during training. The threshold value for clipping gradients is a hyperparameter.
14. **[[Dropout]] and [[Batch Normalization]] Layers**:
    - The dropout rate and other parameters for dropout layers, as well as batch normalization layer settings, are hyperparameters.
15. **Loss Function**:
    - In some cases, the choice of loss function can be a hyperparameter. Different loss functions are suitable for different types of tasks (e.g., mean squared error for regression, cross-entropy for classification).