# HR_Analytics_Retention_Model
HR Analytics: Employee Attrition Prediction Machine learning model to predict employee turnover. Features full preprocessing pipeline (Pandas/Sklearn) and threshold optimization to balance intervention costs vs. retention ROI. Built in Python/Colab.

Employee Attrition Prediction: Retention Strategy with Machine Learning 🚀
This project applies Data Science and Machine Learning to predict employee turnover (churn), enabling HR departments to make data-driven decisions to retain talent and reduce operational costs.

📊 Dataset Overview
The dataset contains detailed information regarding employee profiles, including:

Demographics: Age, marital status, and educational level.

Professional History: Years at company, years in current role, and number of companies worked for.

Satisfaction and Engagement: Job satisfaction level, project involvement, and work-life balance.

Target Variable (Attrition): Indicates whether the employee left the company or not.

🎯 Objective
The main focus is to identify employees most likely to resign. With this information, the company can act proactively, offering personalized benefits or career plans to high-risk profiles.

🛠️ Development and Analysis
The project was structured into a robust processing pipeline:

Automated Preprocessing: I used ColumnTransformer and Pipeline to ensure that new data undergoes the same treatment without data leakage.

Data Handling:

Numerical: Imputation of missing values using the median.

Categorical: Transformation of text into numerical data using TargetEncoder, capturing the relationship between the category and the attrition rate.

Data Splitting: Strict separation between training and testing sets (80/20) with a fixed random_state to ensure experiment reproducibility.

🤖 Machine Learning Models and Optimization
A Logistic Regression model was implemented. To enhance performance, advanced techniques were applied:

Class Weights: Since attrition data is generally imbalanced (fewer people leave than stay), I used compute_class_weight to penalize errors on the minority class. This "forces" the model to pay more attention to cases where employees actually resign.

Evaluation Metrics: In addition to accuracy, the model was evaluated using Precision, Recall, F1-Score, and ROC AUC, ensuring a 360-degree view of performance.

⚖️ Final Insight: The HR Context Trade-off
The most strategic part of this project was the Threshold Analysis. I demonstrated that the model's real-world success depends on an economic balance:

Focus on Recall: Identifies almost all employees at risk, but increases costs by offering benefits to those who might not have left anyway (False Positives).

Focus on Precision: Saves resources by intervening only in high-certainty cases, but runs the risk of losing valuable talent by not detecting them (False Negatives).

Conclusion: Fine-tuning the model allows the company to decide the ideal point of retention investment versus the cost of replacing a vacancy, transforming the predictive model into a financial tool.
