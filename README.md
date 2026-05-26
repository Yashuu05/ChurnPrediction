# Telco Customer Churn Prediction

## 1. Project Overview
The Telco Customer Churn Prediction project leverages machine learning to forecast whether a customer will discontinue their service. By analyzing customer demographics, account information, and service usage patterns, this project aims to provide actionable insights to improve customer retention.

## 2. Problem Statement
Customer churn is a critical issue for telecommunication companies, leading to significant revenue loss. Identifying customers who are likely to churn before they actually do allows businesses to proactively engage with them through targeted retention strategies.

## 3. Objectives
- To build a robust predictive model that accurately classifies customers as likely to churn or not.
- To identify the key features and behaviors that contribute most significantly to customer churn.
- To evaluate multiple machine learning algorithms and select the best-performing model based on evaluation metrics.
- To provide a scalable framework for integrating the model into a production environment.

## 4. Expected Outcome
The expected outcome is a trained machine learning model capable of predicting customer churn with high accuracy and reliability. Additionally, the project will yield insights into customer behavior, helping the business design better retention campaigns and reduce overall churn rates.

## 5. Proposed Solution
The proposed solution involves an end-to-end machine learning pipeline:
1. **Data Preprocessing**: Handling missing values, encoding categorical variables, and scaling numerical features.
2. **Feature Selection**: Using statistical methods and model-based feature importance to select the most relevant predictors.
3. **Model Training & Evaluation**: Training multiple models (Logistic Regression, Random Forest, XGBoost, LightGBM) and evaluating them using metrics like ROC-AUC, F1-score, Precision, and Recall.
4. **Hyperparameter Tuning**: Optimizing the best models using RandomizedSearchCV.
5. **Model Deployment**: Building an API using Flask to serve predictions.

## 6. Tech Stack
- **Programming Language**: Python
- **Data Manipulation & Analysis**: Pandas, NumPy
- **Data Visualization**: Matplotlib, Seaborn
- **Machine Learning**: Scikit-Learn, XGBoost, LightGBM, Imbalanced-learn (SMOTE)
- **Model Tracking & Experimentation**: MLflow
- **Web Framework**: Flask
- **Model Interpretability**: SHAP
- **Database**: PyMongo
- **Environment Management**: python-dotenv

## 7. Hardware and Software Requirements
- **Hardware**: A standard modern computer (minimum 8GB RAM recommended).
- **Software**:
  - Python 3.8+
  - Git
  - Docker (optional, for containerization)
  - Jupyter Notebook (for exploration)

## 8. About the Dataset
The project uses the "Telco-Customer-Churn" dataset.
- **Source**: Kaggle / IBM Telco dataset.
- **Features**: Includes customer demographics (gender, senior citizen status), account information (tenure, contract type, payment method, monthly charges), and services signed up for (phone, internet, streaming).
- **Target Variable**: `Churn` (Yes/No indicating whether the customer left within the last month).

## 9. Machine Learning Algorithms Used
- Logistic Regression
- Random Forest
- XGBoost
- LightGBM

## 10. Results and Performance
Based on the experimental runs, the models were evaluated primarily on the ROC-AUC and F1-score metrics.
- **Random Forest**: Best performing model with a ROC-AUC of ~0.841 and F1-score of ~0.841.
- **XGBoost**: ROC-AUC of ~0.835, F1-score of ~0.835.
- **LightGBM**: ROC-AUC of ~0.833, F1-score of ~0.833.
- **Logistic Regression**: ROC-AUC of ~0.805, F1-score of ~0.806.

The Random Forest model demonstrated the highest overall performance and is selected as the primary model for deployment.

## 11. How to Clone the Repository
To run this project locally, follow these steps:
```bash
# Clone the repository
git clone <repository_url>

# Navigate to the project directory
cd <project_directory>

# Install the required dependencies
pip install -r requirements.txt
```

## 12. Acknowledgement
- Thanks to Kaggle and IBM for providing the open-source Telco Customer Churn dataset.
- The open-source community for the tools and libraries used in this project.

## 13. Conclusion
This project successfully demonstrates the application of machine learning in solving a real-world business problem. By accurately predicting customer churn, telecommunication companies can take proactive measures to retain customers, thereby maximizing revenue and improving customer satisfaction. The use of MLflow ensures reproducibility, while SHAP provides interpretability to the model's predictions.