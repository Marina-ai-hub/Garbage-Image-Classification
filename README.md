# Garbage-Image-Classification
Garbage Image Classification

Built a convolutional neural network (CNN) to classify RGB garbage images by category using TensorFlow and Keras. Explored the impact of convolutional layer parameters (padding, stride, kernel size) on model performance. Tested multiple architectures with convolutional, normalization, and dropout layers. For comparison, also trained a multilayer perceptron (MLP) using scikit-learn.

**Data Source:** Garbage Classification Dataset, Kaggle: https://www.kaggle.com/datasets/asdasdasasdas/garbage-classification

**Results:**
Tthe final model has three convolutional layers, supplemented with one normalization layer, dropout (rate=0.3) and maxpooling layers. After the convolutional layers, there are fully connected layers: with ReLU activation, and the output with SoftMax activation. The results of the model are as follows:
* Early stop at 20/40 epochs
* Validation Loss: 0.77 | Test Loss: 0.87
* Validation Accuracy: 72.41% | Test Accuracy: 70.31%
* Validation Precision: 83.45% | Test Precision: 88.37%
* Validation Recall: 62.86% | Test Recall: 49.48%
* Validation AUC: 94% | Test AUC: 93

Such low accuracy rates and high loss functions may indicate the need for better data balancing, or the introduction of additional filters that will not complicate the model architecture.

For comparison, a multilayer perceptron (MLP) model was also implemented using MLPClassifier from the sklearn library. The model showed significantly lower results:
* Validation Accuracy: 57%  |  Test  Accuracy: 53%
* Validation Precision: 58%  |   Test  Precision: 53%
* Validation Recall: 57%   |   Test  Recall: 53%
* Validation AUC: 82%   |   Test  AUC: 80%
* Validation F1-score: 57%   |   Test  F1-score: 53%
