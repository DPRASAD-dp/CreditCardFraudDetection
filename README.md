# CreditCardFraudDetection
Implemented a hybrid approach combining Logistic Regression and LSTM models for robust credit card fraud detection, achieving high accuracy and performance on imbalanced transaction datasets balanced using SMOTE and ENN.

# Dataset

The dataset used in this project is creditcard.csv, which contains the following columns:

Time: Number of seconds elapsed between this transaction and the first transaction in the dataset.
V1 to V28: Result of a PCA transformation to anonymize the data.
Amount: Transaction amount.
Class: Target variable (1 for fraudulent transactions, 0 for non-fraudulent transactions).

Access the Dataset from this link : https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

# Notebook Structure

Introduction:
Overview of the problem and project objectives.

Data Exploration:
Load and examine the dataset.
Visualize data distributions and correlations.

Data Preprocessing:
Handle missing values.
Normalize the data.

Resampling:
Apply techniques such as SMOTE (Synthetic Minority Over-sampling Technique) and EditedNearestNeighbours to balance the dataset.

Model Training:
Train various machine learning models on the resampled data.
Models used: Logistic Regression and LSTM (Long Short-Term Memory) ensemble model with attention mechanism.

Logistic Regression Model:
Preprocessing: Uses ColumnTransformer to apply transformations.
Model Definition: Logistic Regression is defined in a Pipeline.
Training: Model is trained on the preprocessed data.
Prediction: Predictions are made on the test set.

LSTM Model:
Model Definition: A Sequential LSTM model with:
LSTM Layer
Dropout Layer
Dense Layer
Compilation: Compiled with Adam optimizer and binary cross-entropy loss.
Training: Trained with a learning rate schedule using LearningRateScheduler.
Prediction: Predictions are made and converted to binary format.

Ensemble Method:
Concatenation: Predictions from LR and LSTM models are concatenated.
Attention Mechanism: Applies attention to weight the predictions from each model.
Ensemble Prediction: Weighted predictions are summed and converted to binary format.

Evaluation:
Evaluation metrics include accuracy, ROC AUC, confusion matrix, and classification report for the ensemble model.



