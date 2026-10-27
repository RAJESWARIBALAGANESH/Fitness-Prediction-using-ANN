Fitness Outcome Prediction with an Artificial Neural Network

A binary classification project that uses lifestyle data to predict whether a person is likely to achieve a weight loss goal. The model takes diet score, exercise hours, sleep hours, and stress level as inputs and predicts **Weight Loss** or **Weight Gain**.

## Problem Statement

Can lifestyle habits help predict weight loss outcomes? This project uses the `fitness.csv` dataset to train an Artificial Neural Network (ANN) for this task.

## Tools and Libraries

- Python
- Pandas and NumPy
- TensorFlow/Keras
- scikit-learn

## Features and Target

**Input features:** `Diet_score`, `Exercise_hours`, `Sleep_hours`, and `Stress_level`  
**Target:** `Weight_loss`, mapped as `Weight Loss` → `1` and `Weight Gain` → `0`

## How It Works

1. Load the dataset from `fitness.csv` with Pandas.
2. Select the four lifestyle features and encode the target labels.
3. Split the data into training and test sets (80/20, with `random_state=42`).
4. Standardize the features with `StandardScaler`, fitting the scaler only on the training data.
5. Build and train a Keras Sequential ANN with four ReLU hidden layers (8, 8, 4, and 4 units) and a sigmoid output layer.
6. Train for 100 epochs using the Adam optimizer and binary cross-entropy loss.
7. Evaluate accuracy on the held-out test set and accept interactive lifestyle values for a prediction.

The interactive prediction prints the predicted probability and classifies values at a 0.5 threshold as **Likely to Achieve Weight Loss** or **Unlikely to Achieve Weight Loss**.

## What I Learned

- Preparing features and labels for binary classification
- Splitting data and scaling features without fitting on the test set
- Building and training a multilayer ANN with Keras
- Evaluating a model and using it for interactive predictions

