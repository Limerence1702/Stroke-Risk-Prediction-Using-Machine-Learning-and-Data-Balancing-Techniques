# Stroke-Risk-Prediction-Using-Machine-Learning-and-Data-Balancing-Techniques
This project focuses on building and evaluating machine learning models to predict stroke risk based on clinical and lifestyle-related features. Stroke is one of the leading causes of death and long-term disability worldwide, making early risk detection a critical task in healthcare.
The main objective of this project is not only to build a high-performing predictive model, but also to systematically analyze the impact of different data balancing techniques and machine learning algorithms on imbalanced medical data.

Objectives
- Develop machine learning models to predict stroke risk.
- Handle severe class imbalance using various balancing techniques.
- Compare model performance across multiple algorithms and balancing strategies.
- Prioritize recall as the primary evaluation metric due to the medical context.
- Analyze model behavior in terms of generalization, overfitting, and underfitting.

Dataset Description
Source: https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset
Target Variable: stroke (binary: 1 = stroke, 0 = non-stroke)
Features include:
- Age
- Gender
- Hypertension
- Heart disease
- Average glucose level
- BMI
- Smoking status
- Work type
- Marital status
- Residence type

Dataset Characteristics
- Highly imbalanced target distribution (stroke cases < 5%).
- Presence of missing values (notably in BMI).
- Numerical features with skewed distributions and outliers.

Exploratory Data Analysis (EDA)
EDA was conducted to understand:
- Target class distribution.
- Feature distributions and potential outliers.
- Missing values and data quality issues.
- Relationships between clinical variables and stroke occurrence.

Key findings:
- Severe class imbalance strongly affects naive model performance.
- Numerical features such as glucose level and BMI are right-skewed.
- Median imputation is more suitable than mean for handling outliers.

Data Balancing Techniques
To address class imbalance, multiple techniques were applied and compared:
- Oversampling
- Random OverSampling (ROS)
- SMOTE
- ADASYN
- Undersampling
- Random UnderSampling (RUS)
- Condensed Nearest Neighbour (CNN)
- Neighbourhood Cleaning Rule (NCR)
Hybrid Methods
- SMOTE + NCR
- ADASYN + NCR
The goal is to evaluate how each technique affects model sensitivity to the minority class.

