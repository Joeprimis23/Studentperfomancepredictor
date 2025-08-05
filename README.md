# Studentperfomancepredictor
Student Performance Prediction
Project Overview
This project focuses on building and evaluating machine learning models to predict student academic performance. Using a dataset of student information, the goal is to predict whether a student will pass or fail a final subject based on various demographic, social, and study-related features.

The project demonstrates a complete machine learning workflow, including:

Data loading and exploratory data analysis (EDA).

Feature engineering and preprocessing (creating a binary target, one-hot encoding).

Training and evaluating several classification models.

Identifying the best-performing model.

Saving the final model for future use.

Dataset
The dataset used in this project is student-mat.csv, which contains student performance data in a math course. The data includes 33 features, such as:

Demographics: school, sex, age, address, famsize, Pstatus

Family Information: Medu, Fedu, Mjob, Fjob, reason, guardian

School-related: traveltime, studytime, failures, schoolsup, famsup, paid, activities, nursery, higher, internet, romantic

Lifestyle: famrel, freetime, goout, Dalc (weekday alcohol consumption), Walc (weekend alcohol consumption), health, absences

Grades: G1 (first period grade), G2 (second period grade), G3 (final grade)

Methodology
1. Data Preprocessing

The initial step involved preparing the data for model training:

A new binary target variable, pass, was created. A student was marked as "pass" (1) if their G3 (final grade) was 10 or higher, and "fail" (0) otherwise.

The original G3 column was dropped from the features to prevent data leakage.

Categorical features were converted into numerical format using one-hot encoding.

The data was split into a training set (80%) and a testing set (20%).

2. Model Evaluation

The project evaluated the performance of several popular classification algorithms:

Naive Bayes

Decision Tree

K-Nearest Neighbors (KNN)

Random Forest

XGBoost

Each model's performance was measured using accuracy and a classification report (which includes precision, recall, and F1-score).

3. Key Results

The Random Forest Classifier was found to be the best-performing model for this task, achieving an accuracy of approximately 92.4% on the test set.

4. Feature Importance

An analysis of the Random Forest model's feature importances was conducted to identify the most influential factors in predicting student performance. The results showed that features like G1 (first period grade) and G2 (second period grade) were among the most important predictors, which is a logical and expected outcome.

5. Saving the Model

The final trained RandomForestClassifier and the list of feature column names were saved using the pickle library. This allows the model to be loaded and used for new predictions without needing to be retrained.
