# Stroke-Risk-Prediction-Using-Machine-Learning-and-Data-Balancing-Techniques
This project focuses on building and evaluating machine learning models to predict stroke risk based on clinical and lifestyle-related features. Stroke is one of the leading causes of death and long-term disability worldwide, making early risk detection a critical task in healthcare. The main objective of this project is not only to build a high-performing predictive model, but also to systematically analyze the impact of different data balancing techniques and machine learning algorithms on imbalanced medical data.

## Objectives
- Develop machine learning models to predict stroke risk.
- Handle severe class imbalance using various balancing techniques.
- Compare model performance across multiple algorithms and balancing strategies.
- Prioritize recall as the primary evaluation metric due to the medical context.
- Analyze model behavior in terms of generalization, overfitting, and underfitting.

## Dataset Description
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

## Dataset Characteristics
- Highly imbalanced target distribution (stroke cases < 5%).
- Presence of missing values (notably in BMI).
- Numerical features with skewed distributions and outliers.

## Exploratory Data Analysis (EDA)
EDA was conducted to understand:
- Target class distribution.
- Feature distributions and potential outliers.
- Missing values and data quality issues.
- Relationships between clinical variables and stroke occurrence.

## Key findings:
- Severe class imbalance strongly affects naive model performance.
- Numerical features such as glucose level and BMI are right-skewed.
- Median imputation is more suitable than mean for handling outliers.

## Data Balancing Techniques
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

## Machine Learning Models
Four classification algorithms were evaluated:
1. Logistic Regression
- Used as a baseline model.
- High interpretability and stability.
- No hyperparameter tuning applied.

2. Decision Tree
- Captures non-linear relationships.
- Prone to overfitting without control.

3. Random Forest
- Ensemble of decision trees.
- Reduces variance and improves robustness.
- Hyperparameter tuning applied.

4. XGBoost
- Gradient boosting-based ensemble model.
- High performance on tabular data.
- Includes regularization to control overfitting.

## Evaluation Metrics
The following metrics were used:
- Recall (primary metric)
- Precision
- F1-score
- ROC-AUC
Why Recall?
In medical prediction tasks, false negatives are more dangerous than false positives. Failing to detect a stroke case may have severe consequences, whereas false positives can be handled with further medical examinations.

## Model Evaluation and Analysis
Confusion matrices were used to analyze error types.
Learning curves were generated to assess overfitting and underfitting.
Model performance was compared across all balancing techniques.

## Key observations:
Simple models (Logistic Regression, Decision Tree) achieved higher recall in several scenarios.
Complex models (Random Forest, XGBoost) showed strong ROC-AUC but tended to overfit.
No single balancing technique worked best for all algorithms.

## Limitations
- Dataset size is relatively limited.
- Data originates from a single source.
- Synthetic data generation may not fully reflect real-world medical patterns.
- No external validation dataset was used.

## Future Work
- Incorporate larger and multi-source datasets.
- Explore cost-sensitive learning.
- Apply explainability methods such as SHAP.
- Evaluate model performance in real clinical settings.
