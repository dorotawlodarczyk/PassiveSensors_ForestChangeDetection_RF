README for Step7_RandomForestModelBuilding

Overview
Training and Evaluating a Random Forest Classifier for Image Classification
This script focuses on the application of a Random Forest classifier for image classification tasks. It involves pre-processing training data, training the Random Forest model with specified hyperparameters, evaluating its performance through metrics like confusion matrices and classification reports, and finally, saving the trained model for future use. The process aims to classify images into distinct categories based on extracted feature values, addressing common challenges in geospatial and remote sensing data analysis.

Requirements
Python 3.x
Libraries: numpy, pandas, seaborn, matplotlib, sklearn, pickle
A CSV file containing training samples with extracted feature values

Installation
Ensure Python 3.x is installed on your system. Install the required Python libraries using pip:
pip install numpy pandas seaborn matplotlib scikit-learn

Usage
Random Forest Model Training and Evaluation
1. Cleans training data by handling missing values and infinity.
2. Calculates the distribution of image classes within an Area of Interest (AOI).
3. Trains a Random Forest classifier using the cleaned dataset.
5. Evaluates the model's performance using confusion matrices and classification reports.
6. Saves the trained model to disk for future application.

Key Functionalities
Data Pre-processing: Cleans the training dataset by replacing infinite values with NaN and dropping any rows with missing values.
Training Data Analysis: Calculates and displays the distribution of each class within the training dataset, aiding in understanding the composition of training data.
Model Training: Utilizes the RandomForestClassifier from scikit-learn to train the model with balanced class weights and a specified number of estimators.
Performance Evaluation: Generates a confusion matrix and classification report to assess the model's accuracy and other metrics.
Model Saving: The trained model is serialized using pickle and saved to a specified location for later use.

Output
Trained Random Forest Model: A saved model file (.sav) containing the trained Random Forest classifier.
Confusion Matrix: A graphical representation of the model's performance across the different classes, saved as a PNG file.
Classification Report: A detailed report showing precision, recall, F1-score, and support for each class.

Additional Notes
Before running the script, ensure paths for the training samples CSV file (training_samples.csv), model save location (RF_model.sav), and confusion matrix output (RF_confusion_matrix.png) are correctly set.
The script's performance may vary based on the size and quality of the training data, as well as the specified hyperparameters for the Random Forest model.
Consider experimenting with different hyperparameters and class_weight options to optimize the model for your specific dataset.