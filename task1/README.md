# CNN-based Image Classifier and GAN-based Image Generator

## Overview
This project consists of two main components: an image classifier built using a Convolutional Neural Network (CNN) and an image generator implemented with a Generative Adversarial Network (GAN). The implementation leverages TensorFlow and Keras for deep learning model development.

## Approach

### 1. CNN-based Image Classifier
The classifier is a CNN trained on a given dataset to recognize and categorize images. The steps for constructing the CNN are:

- **Data Preprocessing**: Load and normalize the dataset.
- **Model Architecture**: Design a CNN with convolutional, pooling, and fully connected layers.

#### Model: "sequential"

| Layer (type)                   | Output Shape         | Param #       |
|--------------------------------|----------------------|--------------|
| conv2d (Conv2D)                | (None, 348, 348, 64) | 1,792        |
| max_pooling2d (MaxPooling2D)   | (None, 174, 174, 64) | 0            |
| conv2d_1 (Conv2D)              | (None, 172, 172, 128)| 73,856       |
| max_pooling2d_1 (MaxPooling2D) | (None, 86, 86, 128)  | 0            |
| conv2d_2 (Conv2D)              | (None, 84, 84, 256)  | 295,168      |
| max_pooling2d_2 (MaxPooling2D) | (None, 42, 42, 256)  | 0            |
| flatten (Flatten)              | (None, 451584)       | 0            |
| dense (Dense)                  | (None, 256)         | 115,605,760  |
| dense_1 (Dense)                | (None, 1)           | 257          |

**Total params:** 115,976,833 (442.42 MB)  
**Trainable params:** 115,976,833 (442.42 MB)  
**Non-trainable params:** 0 (0.00 B)

- **Compilation and Training**: Compile the model using categorical cross-entropy loss and train it with the Adam optimizer.
- **Evaluation**: Assess performance on the validation/test set using accuracy and loss metrics.

### 2. GAN-based Image Generator
A GAN is used to generate synthetic images. The approach includes:

#### GAN Architecture:
- **Generator**: A deep neural network that learns to create realistic images.
- **Discriminator**: A CNN that distinguishes between real and generated images.

#### Training the GAN:
- The generator and discriminator are trained adversarially.
- The discriminator learns to distinguish real from fake images.
- The generator is trained to produce realistic images that can fool the discriminator.

### Generating Synthetic Images
Once trained, the generator produces new images that can be used for various applications.
