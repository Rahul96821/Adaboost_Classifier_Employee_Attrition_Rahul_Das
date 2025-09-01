HR Employee Attrition Prediction:

Project Overview:

Employee attrition is a major concern for organizations, as losing valuable employees can increase recruitment costs, disrupt team dynamics, and impact overall productivity. Predicting employee attrition helps HR departments take proactive measures to retain talent and maintain organizational stability.

This project aims to build a machine learning model that predicts whether an employee is likely to leave the organization based on historical HR data, including demographic, job-related, and workplace information.

Dataset:

The dataset used contains 1470 employee records with 35 features, including:

Numerical Features: Age, DailyRate, DistanceFromHome, TotalWorkingYears, YearsAtCompany, etc.

Categorical Features: Department, JobRole, BusinessTravel, OverTime, MaritalStatus, etc.

The target variable is Attrition (Yes/No).

Data Preprocessing:

Separation of features: Numeric and categorical features were handled separately.

Scaling: Numeric features were standardized using StandardScaler.

Encoding: Categorical features were one-hot encoded using pd.get_dummies.

Feature set creation: The processed numeric and categorical features were combined into a single dataset for modeling.

Modeling:

Algorithm: AdaBoost Classifier

Hyperparameters: n_estimators=200, random_state=100

Train/Test Split: 70% training, 30% testing

The model predicts the likelihood of an employee leaving (attrition) or staying.

Results

Accuracy: 86.4%

Confusion Matrix:

[[355, 16],
 [ 44, 26]]


Interpretation:

The model predicts non-attrition cases (employees staying) very accurately.

Prediction for actual attrition cases (employees leaving) is slightly lower, likely due to class imbalance in the dataset.

Conclusion:

The AdaBoost model successfully identifies employees at risk of leaving, providing actionable insights for HR to implement retention strategies. Future improvements could include:

Handling class imbalance using techniques like SMOTE

Feature selection and dimensionality reduction

Testing alternative models such as Random Forest, XGBoost, or Gradient Boosting
