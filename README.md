# Diabetes Prediction Model

This repository contains a machine learning-based diagnostic model designed to predict the likelihood of an individual having diabetes, based on behavioral and health parameters. The project also explores the business potential and healthcare impact of deploying such predictive tools.

## Objective

To develop a predictive model that forecasts a patient’s likelihood of having diabetes (including prediabetes) using survey data from the CDC’s Behavioral Risk Factor Surveillance System (BRFSS).

---

## Dataset

- **Source**: https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset
- **Size**: 253,680 survey responses
- **Target Variable**: `Diabetes_012`
  - `0`: No diabetes or only during pregnancy  
  - `1`: Prediabetes  
  - `2`: Diabetes
- **Features**: 21 predictors including BMI, smoking status, physical activity, general health rating, and more.
- **Note**: There is a class imbalance in the dataset which impacts model performance, especially for minority classes.

---

## Methodology

Multiple classification models were developed and evaluated:
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost

Evaluation was performed using metrics such as ROC AUC to compare both training and test performances.

---

## Results

| Model               | Training AUC | Test AUC | Notes |
|---------------------|--------------|----------|-------|
| Decision Tree       | 0.90         | 0.62     | Overfitting observed |
| Logistic Regression | —            | 0.73     | Best generalization |
| XGBoost             | —            | Low      | Underperformed, requires tuning |

- Most models performed best at predicting class `0` (non-diabetic).
- Indicates potential need for data augmentation or balancing techniques for under-represented classes.

---

## Business Value

### Market Opportunity
- **U.S. Population Impacted**:
  - 34M with diabetes
  - 88M with prediabetes
- **Subscription Model**:
  - $10/month × 1% of prediabetes population = **$105M annual revenue**
- **Enterprise Licensing**:
  - 1,000 providers × $10,000/year = **$10M/year additional revenue**

### Cost Savings
- **Average annual diabetes care cost**: $16,750
- **Savings if 1% of prediabetics avoid diabetes**:  
  880,000 people × $9,600/year = **$8.4B/year**

---

## Risks and Limitations

- **Prediction Accuracy**: False positives/negatives can have serious medical implications.
- **Data Privacy**: Sensitive health data must comply with regulations like HIPAA.
- **Ethical Concerns**: Risk of discrimination in insurance or employment.
- **Over-reliance**: Tools must assist—not replace—medical judgment.

---

## Benefits

- **Early Intervention**: Supports proactive health planning and prevention.
- **Personalized Care**: Enables tailored treatment and lifestyle changes.
- **Public Health Insights**: Contributes to research and policy planning.
