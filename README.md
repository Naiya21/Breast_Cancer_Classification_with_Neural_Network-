# Breast Cancer Classification using Neural Networks

This project implements a Neural Network model using TensorFlow and Keras to classify breast cancer as **Malignant** or **Benign**. The dataset used is the Breast Cancer Wisconsin dataset provided by sklearn. The aim is to predict whether a tumor is malignant or benign based on features like cell radius, texture, perimeter, and area.

## Dataset

The dataset used in this project is the **Breast Cancer Wisconsin** dataset from `sklearn.datasets`. It consists of 569 instances of tumors, with 30 features each, and a binary target:
- **0**: Malignant (cancerous)
- **1**: Benign (non-cancerous)

## Project Structure

The project involves the following steps:

1. **Data Loading and Exploration**:
   - Load the dataset using sklearn.
   - Explore the data and create a pandas DataFrame to view the feature names and target labels.
   - Analyze the distribution of the target variable and compute mean values for each label class.

2. **Data Preprocessing**:
   - The data is split into features (`X`) and labels (`Y`).
   - Standardization is applied using `StandardScaler` to scale the features.

3. **Model Creation**:
   - A sequential neural network model is built using Keras. The model consists of:
     - `Flatten` layer to convert the input into a 1D array.
     - Two `Dense` layers:
       - One hidden layer with 20 neurons and ReLU activation.
       - Output layer with 2 neurons and sigmoid activation for binary classification.
   
4. **Model Compilation & Training**:
   - The model is compiled using the Adam optimizer and sparse categorical cross-entropy loss.
   - The model is trained on the training data for 10 epochs with validation data split.

5. **Evaluation & Prediction**:
   - Model performance is evaluated using test data, and accuracy is calculated.
   - Predictions are made on new data points, and the predicted class label is printed.
 
