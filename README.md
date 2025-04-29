# Task4
 Logistic Regression for Heart Disease Prediction
Objective:
The goal of this task was to build a binary classification model using logistic regression to predict whether an individual will develop coronary heart disease (CHD) within the next 10 years. The target variable for prediction was TenYearCHD, which is either 0 (no disease) or 1 (disease present).

Dataset Overview:
The dataset contained health-related data of individuals with features such as:
Demographics: age, gender, education
Lifestyle: smoking status, cigarettes per day
Medical history: diabetes, blood pressure medication, previous strokes
Clinical measurements: cholesterol levels, systolic/diastolic blood pressure, BMI, heart rate, glucose levels
The target column was TenYearCHD, indicating if heart disease occurred within a 10-year window.

Step 1: Data Cleaning
I started by checking the dataset for missing values and removed any incomplete records to ensure the model could be trained without errors. I also reviewed the data types and ensured all features were suitable for modeling.

 Step 2: Feature Selection and Target Definition
All columns except TenYearCHD were treated as input features. The TenYearCHD column served as the target variable we wanted to predict.

Step 3: Train-Test Split
To evaluate the model properly, I split the dataset into two parts:
80% for training the model
20% for testing the model's performance
This helps simulate how the model would perform on new, unseen data.

Step 4: Feature Standardization
Since the features had different scales (like age, cholesterol, and glucose), I standardized them to ensure that each feature contributed equally to the model. This is especially important for logistic regression, which is sensitive to feature scale.

Step 5: Logistic Regression Model Training
I used logistic regression for this classification task. Logistic regression is appropriate because it is designed to predict probabilities between 0 and 1 using the sigmoid function. Based on these probabilities, it assigns a class label (0 or 1).

Step 6: Model Evaluation
Once the model was trained, I evaluated its performance using the following metrics:
Confusion Matrix: Showed how many cases were correctly or incorrectly classified.
Precision: Measured how many of the predicted positives were actually correct.
Recall: Measured how many actual positive cases the model was able to identify.
ROC-AUC Score: Gave an overall measure of the model’s performance in distinguishing between classes.
These metrics helped understand both the accuracy and reliability of the model.

Step 7: Threshold Tuning
By default, logistic regression uses a threshold of 0.5 to classify outcomes. However, in medical problems like heart disease, it can be more useful to lower the threshold (for example, to 0.3) to catch more true cases, even if it means slightly more false positives. I experimented with different thresholds to improve the recall, which is important for early disease detection.

Step 8: ROC Curve Visualization
I plotted the ROC curve, which shows the trade-off between the true positive rate and false positive rate across different thresholds. A model with a curve closer to the top-left corner is considered more effective.

 Sigmoid Function (Explanation)
The logistic regression model uses a mathematical function called the sigmoid function to map any input value into a probability between 0 and 1. This helps in deciding whether a prediction should be classified as 0 (no heart disease) or 1 (at risk of heart disease). The sigmoid curve is S-shaped, and the threshold determines at what point a person is labeled as high risk.

Additional Enhancements (Optional/For Extra Credit)
To further improve the project, I explored:
Feature importance to understand which variables had the most influence on heart disease.
Class imbalance handling to adjust for the fact that fewer people in the dataset had heart disease (this improves the model's sensitivity).
Alternative classifiers like Random Forest for comparison.
Threshold optimization plots to find the best balance between precision and recall.

Conclusion
Through this task, I successfully built a binary classification model using logistic regression. I followed a structured approach: cleaning the data, preparing features, training the model, evaluating it with key metrics, tuning thresholds, and interpreting results. This allowed me to identify individuals who are at risk of developing heart disease, making this model useful for preventive healthcare applications.

