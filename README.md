# Credit-Card-Fraud-Detection

## 📂 Dataset

This project uses a publicly available dataset from Kaggle:  
👉 [Credit Card Fraud Detection Dataset on Kaggle](https://www.kaggle.com/datasets/kartik2112/fraud-detection)

Please download the dataset manually from Kaggle and upload it into the notebook when prompted.

This notebook demonstrates how to detect credit card fraud by building, selecting, and evaluating machine learning models, with fast experimentation using PyCaret.
It also includes fraud analysis based on transaction categories and gender distribution.

Project Workflow
1. Install & Import Libraries
Install necessary libraries (PyCaret, pandas, etc.)

Import modules for machine learning, visualization, and file handling.

2. Upload Data
Upload separate training and testing datasets manually.

Load datasets into pandas DataFrames.

3. Preprocessing
Drop irrelevant columns like Unnamed: 0, first, last, street, trans_num, dob.

Extract useful datetime features: hour, day, weekday, month from trans_date_trans_time.

Create a smaller sample of 20,000 rows for faster initial model testing.

4. Setup PyCaret
Use PyCaret's setup() function to initialize the environment:

Normalize data

Handle class imbalance

Remove multicollinearity

5. Model Comparison
Compare fast classifiers: Random Forest, XGBoost, LightGBM, CatBoost, Extra Trees.

Rank models based on Recall (priority: catch as many frauds as possible).

Allow manual selection of the preferred model.

6. Final Training
Re-train the selected model on the full training dataset using the same preprocessing settings.

Finalize the model for deployment.

7. Model Evaluation
Predict on the uploaded test dataset.

Evaluate model performance using:

Classification Report (Precision, Recall, F1-score)

Confusion Matrix (True Positive, False Positive rates)

ROC AUC Score (if available)

8. Feature Importance
Visualize the top features influencing fraud detection.

9. Fraud Analysis
Analyze fraud concentration across transaction categories:

Display fraud rate by category

Plot the top 10 fraud-prone categories

Analyze fraud distribution across genders:

Pie chart showing male vs female victims.

 Visualizations Included
Confusion Matrix Heatmap

Feature Importance Plot

Bar Chart: Top Categories by Fraud Rate

Pie Chart: Fraud Victims by Gender

Requirements

Library	Version
Python	3.7+
pandas	Latest
numpy	Latest
pycaret	Latest
matplotlib	Latest
seaborn	Latest

Key Takeaways
Fraud datasets are heavily imbalanced — recall is a critical metric.

PyCaret dramatically speeds up model experimentation and tuning.

Fraud analysis by category and gender can give valuable business insights.

Final model selection should be user-driven based on explainability and performance.

Files
train.csv → Training data (with labeled frauds)

test.csv → Testing data (for final evaluation)

Credit_Card_Fraud_Detection.ipynb → This notebook

Future Improvements
Use advanced ensembling/blending models for even better accuracy.

Integrate SHAP values for explainable AI.

Automate hyperparameter tuning with tune_model() in PyCaret.

Deploy as an API for real-time fraud detection.

Results
By using PyCaret and focusing on recall, the best models like Extra Trees or XGBoost can accurately detect fraudulent transactions while minimizing false alarms!

Author
Created by: [Kavish Harpale]
Date: April 2025
