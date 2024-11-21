### Description of the Code

This code evaluates multiple machine learning models for a **customer churn prediction system** by training and testing each model, printing its performance metrics, and summarizing the results.

#### **Steps and Explanation:**

1. **Data Preprocessing**:
   - The dataset is preprocessed (standardized, split into training and test sets).
   - The `X_train` and `X_test` variables hold the features, and `y_train` and `y_test` hold the target labels.

2. **Model Evaluation**:
   - The `evaluate_model` function trains a model, predicts on the test set, and calculates the following metrics:
     - **Accuracy**: The ratio of correctly predicted samples to the total samples.
     - **Confusion Matrix**: A matrix summarizing the number of true positives, true negatives, false positives, and false negatives.
     - **Classification Report**: Provides precision, recall, F1-score, and support for each class.

3. **Model List**:
   - Includes the following algorithms:
     - **Logistic Regression**: A linear model for binary classification.
     - **Naive Bayes**: A probabilistic classifier based on Bayes' theorem.
     - **Support Vector Machine (SVM)**: Finds a hyperplane to separate classes.
     - **Decision Tree**: Uses a tree structure to make predictions based on feature splits.
     - **Random Forest**: An ensemble of decision trees for improved accuracy.
     - **Extra Trees**: A more randomized version of Random Forest.
     - **AdaBoost**: Boosting technique that combines weak learners.
     - **XGBoost**: Gradient boosting algorithm optimized for speed and accuracy.
     - **CatBoost**: Gradient boosting model optimized for categorical data.

4. **Metrics Collection**:
   - Each model is evaluated using `evaluate_model`.
   - The results, including accuracy, confusion matrix, and classification report, are stored in a dictionary for further analysis.

5. **Summary**:
   - The final section prints a summary of the accuracy scores for all models, allowing easy comparison.

#### **Output Example**

For each model, the code outputs:
- **Model Name**: e.g., "Logistic Regression"
- **Accuracy**: e.g., `Accuracy: 0.8490`
- **Confusion Matrix**:
  ```
  [[190   5]
   [ 20  85]]
  ```
- **Classification Report**:
  ```
               precision    recall  f1-score   support
           0       0.90      0.97      0.93       195
           1       0.94      0.81      0.87       105
  ```
- A **Summary Table** of accuracies for all models:
  ```
Summary of Model Accuracies:
Logistic Regression: Accuracy = 0.8490
Naive Bayes: Accuracy = 0.8200
Support Vector Machine: Accuracy = 0.8600
Decision Tree: Accuracy = 0.8350
Random Forest: Accuracy = 0.8700
Extra Trees: Accuracy = 0.8500
AdaBoost: Accuracy = 0.8400
XGBoost: Accuracy = 0.8800
CatBoost: Accuracy = 0.8750

### Purpose

This code:
1. Trains various machine learning models on the churn dataset.
2. Evaluates their performance comprehensively.
3. Helps in selecting the best model based on its accuracy and other metrics.

