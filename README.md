# Project overview
The aim of this project was to build a machine learning model to predict fraudulent credit card transactions. The model was be based on a public dataset available in Kaggle (link to dataset: https://www.kaggle.com/datasets/kelvinkelue/credit-card-fraud-prediction?resource=download).

# Objetives
The goal was set taken into consideration that most trasanctions are non-fraudulent and the performance of baseline models. Regarding transaction, in the dataset used 99.614% of trasanctions are non-fraudulent. Because of this, using accuracy as a metric would be deceiving as any model that predicts all transactions to be non-fraudulent would achieve an accuracy score of 99.614%. Moreove, a simple baseline model was able to reach 99% accuracy and 73% of recall. This means that at least 99% of the predictions made by the baseline modelwere right and it would be able to block 73% of attemps of fraud.

Taking that context into consideration, the goal for this proejct was to build a model that was able to keep 99% accuracy, while reaching a recall of at least 90%. This means that at least 99% of the predictions made by the model have to be right and at least 90% of attemps of fraud will be identified by the model.

# Technologies & Tools
- **Programming Language:** Python
- **Development Environment:** Jupyter Notebook
- **Libraries & Frameworks:**
  - **Data Processing & Analysis:** pandas, numpy, statsmodels
  - **Data Visualization:** matplotlib, seaborn
  - **Modeling and Evalution**: sklearn, imblearn, tensorflow, keras, xgboost
  - **Model Explanation**: shap
 
# Skills employed in the project
- **Data Wrangling & Cleaning:** 
- **Data Visualization:** 
- **Machine learning:** 
- **Report Writing & Documentation:**

# Key Insights

For an visual presentation of the project, visit: https://github.com/diogofn1/Fraud-detection/blob/main/Machine%20Learning%20Project%20-%20Presentation.pdf.
