# Plant Disease CNN Classification

This project builds a Convolutional Neural Network (CNN) to classify plant leaf images into different disease categories using the PlantVillage dataset.

## Project Overview

The model is trained on labeled plant images and learns to identify healthy vs. diseased leaves across multiple classes. The workflow includes:

- downloading the dataset from Kaggle
- loading images with PyTorch
- preprocessing and augmenting the dataset
- training a custom CNN model
- evaluating validation accuracy

## Dataset

The project uses the PlantVillage dataset from Kaggle:

- Dataset: `mohitsingh1804/plantvillage`
- Source: KaggleHub
- Classes: multiple crop and disease categories

The dataset is organized into train and validation folders, and each class is kept in a separate subdirectory.

## Model Architecture

The CNN model includes:

- 3 convolutional blocks
- ReLU activation
- Batch normalization
- Max pooling layers
- Fully connected classifier layers
- Dropout for regularization

This is implemented in the notebook as a custom `MyCNN` class.

## Technologies Used

- Python
- PyTorch
- torchvision
- PIL (Python Imaging Library)
- KaggleHub
- Matplotlib

## Project Files

- `cnn_project.ipynb` – main training and evaluation notebook
- `image.ipynb` – image viewing and preprocessing exploration
- `README.md` – project documentation

## Setup

1. Create and activate a Python environment.
2. Install the required libraries:

```bash
pip install torch torchvision pillow kagglehub matplotlib
```

3. Make sure you have a valid Kaggle API configuration if the dataset is being downloaded from Kaggle.

## Running the Project

Open the notebook `cnn_project.ipynb` and run the cells in order:

1. Install required imports
2. Download the PlantVillage dataset
3. Set the dataset paths
4. Define image transforms
5. Build the custom dataset class
6. Create data loaders
7. Define the CNN model
8. Train the model
9. Evaluate accuracy on validation data

## Training Configuration

The notebook uses:

- device: GPU if available, otherwise CPU
- batch size: 32
- optimizer: Adam
- learning rate: 0.001
- loss function: CrossEntropyLoss
- epochs: 10

## Expected Result

After training, the model outputs validation accuracy and loss values to measure performance on unseen plant disease images.

## Notes

- The project is designed for image classification tasks in plant health monitoring.
- It can be extended with more epochs, data augmentation, transfer learning, or a better pretrained model such as ResNet or EfficientNet.

## Future Improvements

- add data augmentation
- use pretrained CNN models
- improve class balancing
- tune hyperparameters
- save model weights for inference

