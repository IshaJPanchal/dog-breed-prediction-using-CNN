# 🐶 Dog Breed Prediction Using CNN

This project aims to classify dog breeds from images using a Convolutional Neural Network (CNN) built with TensorFlow and Keras. It utilizes a dataset containing images of 70 dog breeds, organized into training, validation, and test sets.

## 📁 Dataset

The dataset is downloaded using [KaggleHub](https://github.com/KaggleHub/kagglehub) from the following source:

- **Dataset**: [70 Dog Breeds - Image Dataset](https://www.kaggle.com/datasets/gpiosenka/70-dog-breedsimage-data-set)
- **Structure**:
  ```
  /train
  /test
  /valid
  ```

Each folder contains subdirectories for each dog breed with corresponding images.

## 🧠 Model Architecture

The CNN model is composed of:

- Data Augmentation layers to avoid overfitting:
  - Horizontal flipping
  - Random rotation
  - Random zoom
- Convolutional and MaxPooling layers:
  - Conv2D with increasing filters: 32 → 64 → 128 → 256 → 512
  - Each followed by MaxPooling2D
- Final layers include:
  - Flatten
  - Dense layers
  - Dropout for regularization
  - Output Dense layer with softmax activation for classification

## 🧪 Training & Validation

- Images are resized to **224x224**
- Batch size is **32**
- Label mode is set to **integer**
- Standard Keras `image_dataset_from_directory()` is used for loading datasets.

## 🛠️ Requirements

- Python 3.8+
- TensorFlow
- Matplotlib
- KaggleHub

Install requirements using:

```bash
pip install tensorflow matplotlib kagglehub
```

## 🚀 How to Run

1. Clone the repository or open the notebook in Jupyter.
2. Make sure your Kaggle API key is set up to use KaggleHub.
3. Run all cells to download the dataset, train the model, and evaluate its performance.

## 📈 Evaluation

The model is trained and validated on the provided sets and evaluated on a separate test set. Augmentation and dropout are used to prevent overfitting and improve generalization.