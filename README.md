# JUNIO ANGELICA-FASHION-MNIST-Image-Classification-2026

##Google colab Link - https://colab.research.google.com/drive/1qB2fgk1KeZTDoiGTkX36DmOBisSshuqG?usp=sharing


###Questions:
What is the Fashion MNIST dataset?
Answer: The MNIST dataset (Modified National Institute of Standards and Technology dataset) is a large, standardized dataset of handwritten digits that is widely -
used in the field of machine learning and computer vision for training and evaluating models. 


Why do we normalize image pixel values before training?
Answer: We normalize image pixel values before training to scale them to a consistent range (usually 0–1), which makes learning faster, more stable, and improves model accuracy.
Normalizing image pixel values before training a machine learning model is an important preprocessing step that significantly improves the model’s performance and stability. 
Most images, including datasets like MNIST, have pixel values ranging from 0 to 255.
If these raw values are fed directly into a neural network, they can cause problems: large input values can lead to unstable gradients, slow convergence during training, and inefficient learning.



List the layers used in the neural network and their functions?
Answer: In a typical neural network for image classification (like MNIST), the layers and their functions are as follows:

1. Input Layer
Function: Receives the raw input data (e.g., a 28×28 pixel image).
Often flattens the image into a 1D vector so it can be processed by the network.
Example: Flatten(input_shape=(28, 28)) converts a 28×28 image into a 784-element vector.

2. Dense (Fully Connected) Layer
Function: Each neuron is connected to all neurons in the previous layer.
Learns features by applying weights and biases to inputs.
Usually uses an activation function like ReLU to introduce non-linearity.
Example: Dense(128, activation='relu') creates 128 neurons with ReLU activation.

3. Hidden Layers
Function: Intermediate layers between input and output.
Extract complex features from the input.
4. Output Layer
Function: Produces the final predictions.
For classification, usually has one neuron per class with a softmax activation to output probabilities.
Example: Dense(10, activation='softmax') outputs probabilities for 10 classes (digits 0–9).
5. Activation Functions (applied in layers)
ReLU (Rectified Linear Unit): Introduces non-linearity, allows the network to learn complex patterns.
Softmax: Converts output scores into probabilities that sum to 1.
Sigmoid / Tanh: Sometimes used in hidden layers for other types of networks


What does an epoch mean in model training?
- An epoch in model training is defined as one complete pass of the entire training dataset through the neural network.
-  During training, data is often divided into smaller batches for efficient processing.
-  The network updates its weights after each batch, and once all batches have been processed, it counts as one epoch.
Training usually requires multiple epochs so the model can gradually learn patterns from the data.
Too few epochs can lead to underfitting, where the model has not learned enough, while too many epochs can cause overfitting, where the model memorizes the training data and performs poorly on new data.
For example, if a dataset has 10,000 images and the batch size is 1,000, one epoch consists of 10 iterations.
 Training the model for 5 epochs means each image in the dataset is seen five times in total, allowing the model to improve its accuracy gradually.

Compare the predicted label and actual label for the first test image.
- To compare the predicted label and actual label for the first test image in a classification task like MNIST, we follow these steps:
Actual label: This is the true digit that the first test image represents, provided in the dataset. For example, it might be 7.

Predicted label: This is the output of the trained model when it processes the first test image. 
The model predicts the digit by selecting the class with the highest probability from the output layer (usually using argmax). For example, the model might predict 7.

Comparison:
If the predicted label matches the actual label, the model has classified the image correctly.
If the predicted label does not match, the model has misclassified the image.




What could be done to improve the model’s accuracy?
Answer: To improve a neural network’s accuracy, several strategies can be applied. Increasing the number of layers or neurons allows the model to learn more complex patterns,
while using regularization techniques like dropout or early stopping helps prevent overfitting and improves generalization. 
Proper data preprocessing, such as normalizing pixel values and applying data augmentation, can make the model more robust. 
Tuning hyperparameters like learning rate, batch size, and optimizer choice, as well as training for more epochs, can also enhance performance.
Additionally, using advanced architectures such as convolutional neural networks (CNNs) and employing better weight initialization and optimization methods can significantly boost accuracy.




Tasks Enhancement:
1. Change the number of neurons in the hidden layer (e.g., 64 or 256) and retrain the model.
2. Increase the number of epochs and observe changes in accuracy.
3. Add another hidden layer and compare the results.
