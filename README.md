# Flight Delay Prediction and Analysis

## 1. Overview

This project performs data cleaning, exploratory data analysis, feature engineering, and machine learning to predict the primary reason for flight delays using a flight dataset.

## 2. Dataset

The dataset is loaded from a CSV file containing flight records with attributes such as date, airline, scheduled times, and delay-related features.

## 3. Data Preprocessing

1. Load dataset using pandas
2. Select relevant columns
3. Check for missing values
4. Remove rows with missing arrival delay
5. Fill missing delay-related values with zero
6. Reduce dataset to relevant features for modeling

## 4. Feature Engineering

1. Create a new column called all_delay as the sum of delay features
2. Create target column delay_reasons
3. Assign NO_DELAY when total delay is zero
4. Otherwise assign the delay type with the highest value
5. Apply one hot encoding to categorical variables

## 5. Data Splitting

1. Split dataset into training, validation, and test sets
2. Use train_test_split from sklearn

## 6. Handling Imbalanced Data

1. Use RandomOverSampler from imblearn
2. Resample training data to balance classes

## 7. Model Training

1. Train DecisionTreeClassifier using training data

## 8. Model Evaluation

1. Predict on test data
2. Compute accuracy score
3. Generate confusion matrix
4. Visualize confusion matrix using seaborn heatmap

## 9. Requirements

Install required libraries using the following command

pip install pandas numpy scikit-learn imbalanced-learn seaborn matplotlib

## 10. Running the Project

1. Place the dataset at the specified file path or update the path in the script
2. Run the Python script or notebook

## 11. Future Improvements

1. Try advanced models such as Random Forest or Gradient Boosting
2. Perform hyperparameter tuning
3. Add feature importance analysis
4. Deploy as a web application
