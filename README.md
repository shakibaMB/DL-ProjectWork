# DL-ProjectWork
This repository provides an implementation for "Diagnosing COVID-19 using the Inception V3 network" task for deep learning course @unibo.

Diagnosing COVID-19 Using the Inception V3 Network

In this project, the diagnosis of COVID-19 from chest CT scan images was accomplished using the Inception V3 neural network. The dataset used in this project consists of two sets of lung images: one from healthy individuals and another from individuals infected with COVID-19.

The dataset contains a total of 576 CT scan images from COVID-19-infected individuals and 1583 CT scan images from healthy individuals. Out of these, 460 images from COVID-19-infected individuals and 1266 images from healthy individuals were used for training the Inception V3 network, while the remaining images were utilized for network testing.

To prepare the dataset for network training, all images were resized to 128x128 pixels. Additionally, since Inception V3 expects RGB images as input, grayscale images in the dataset were converted to RGB format. To ensure image consistency, they were normalized to a range of 0 to 255.

In the network model definition, a convolutional layer was introduced to adapt the network to single-channel images. Several additional layers were added to improve network performance, including zero-padding layers, which are a common type of layer. Dropout layers were also used to prevent overfitting.

The number of classes in the Dense layer was set to 2 due to the two categories of images: healthy individuals and those infected with COVID-19.

Since the project's goal was image classification, the CategoricalCrossentropy loss function was used. The learning rate was set to 0.005 after several evaluations, and a batch size of 8 was chosen.
