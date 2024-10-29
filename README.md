This project implements a convolutional neural network (CNN) for classifying images of cars and trucks using transfer learning with the VGG19 architecture. The model is built using TensorFlow and Keras.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Model Training](#model-training)
- [Evaluation](#evaluation)
- [Functionality](#functionality)
- [License](#license)

## Installation

To run this code, you will need the following libraries:

- TensorFlow
- Keras
- NumPy
- Pillow (PIL)

You can install the required libraries using pip:

```bash
pip install tensorflow numpy pillow
```

## Dataset

The dataset used for training the model consists of images of cars and trucks. Make sure to place the images in the following directory structure:

My Drive/CV992/
    ├── car/
    │   └── <car_image1.jpg>
    │   └── <car_image2.jpg>
    │   └── ...
    └── truck/
        └── <truck_image1.jpg>
        └── <truck_image2.jpg>
        └── ...

        
## Model Training

The model uses the VGG19 architecture with pre-trained weights from ImageNet. The model is fine-tuned on the car and truck dataset. Here are the main steps:

1. Load and preprocess images.
2. Split the dataset into training, validation, and testing sets.
3. Define the VGG19 model and freeze the convolutional layers.
4. Compile the model with the Adam optimizer and binary cross-entropy loss.
5. Train the model and save the best version.


## Evaluation

The trained model is evaluated on the test set, and the accuracy is printed for both training and test datasets.

## Functionality

The function car_truck_classifier(address) takes the path to an image and predicts whether it is a car or a truck. It returns a string indicating the prediction.

Example usage:

```bash
test_img_address = 'path_to_your_image.jpg'
print(car_truck_classifier(test_img_address))
```
