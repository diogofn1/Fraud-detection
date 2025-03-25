# Project overview

The objective of this project was to develop a machine learning model aimed at predicting fraudulent credit card transactions. The model was built using a publicly available dataset from Kaggle (link to dataset: https://www.kaggle.com/datasets/kelvinkelue/credit-card-fraud-prediction?resource=download).

# Objetives
The goal was set taken into consideration that most trasanctions are non-fraudulent and the performance of baseline models. Given the imbalanced nature of the dataset (99.614% of transactions are non-fraudulent), accuracy as a metric would not effectively assess model performance as any model that predicts all transactions to be non-fraudulent would achieve an accuracy score of above 99%. Moreove, a simple baseline model was able to reach 99% accuracy and 73% of recall. This means that at least 99% of the predictions made by the baseline modelwere right and it would be able to block 73% of attemps of fraud.

Taking that context into consideration, the goal for this proejct was to build a model that was able to keep 99% accuracy, while reaching a recall of at least 90%. This means that at least 99% of the predictions made by the model would have to be right and at least 90% of attemps of fraud would be identified by the model.

# Technologies & Tools
- **Programming language:** Python
- **Development environment:** Jupyter Notebook
- **Libraries & frameworks:**
  - **Data processing & analysis:** pandas, numpy, sklearn, SHAP
  - **Data visualization:** matplotlib, seaborn
  - **Modeling and evalution**:  scikit-learn, imbalanced-learn, TensorFlow, Keras, XGBoost
  - **Model explanation**: SHAP
 
# Skills employed in the project
- **Data wrangling:** preprocessing the dataset through data cleaning, transformation, and handling imbalanced data for effective modeling.
- **Data visualization:** visualizing and interpreting the relationships between variables to gain insights into transaction patterns and fraud behavior.
- **Machine learning:** model building to predict which transactions are fradulents or non-fradulent.
- **Model selection**: analyzing performance metrics such as precision, recall, and F1-score to decide on the most suited model to address the problem.
- **Model interpretation & explainability**: using SHAP values and feature importance to explain model predictions, improving transparency and trust in the results.
- **Report writing & documentation:** synthesizing findings and presenting results through detailed visualizations and concise textual summaries to aid data-driven decision-making.

# Key Insights and Model Performance

The best-performing model was XGBoost with the following hyperparameters:
- max_depth=5, learning_rate=0.01, threshold set to 0.7 for fraud prediction.

The model achieved the following results on the test dataset:
- Accuracy: above 99%
- Precision: 29%
- Recall: 92%
- F1-Score: 44%
These results indicate that the model correctly predicted 99% of transactions, while detecting 92% of fraudulent attempts.

The most influential features in the model were:
- **Transaction amount:** typical value for fraudulent transactions is more than 7 times larger than non-fraudulent transactions
- **Transaction time:** most fraudulent transactions happend between 22h and 3h.

This result have to be considered within the context of a company. Even though 92% recall seems to be great at first glance, the business can have an even higher expectation and further exploration of models could be done parameter tuning, trying different kinds of neural networks, and so on.

# Business Implications & Recommendations

In case this model is satisfactory, some final business recomendations would be:

- **Model deployment:** if the model's performance aligns with expectations, it should be deployed to automate fraud detection, potentially preventing 92% of fraudulent transactions.
- **Model validation:** real-world testing should be conducted to confirm whether the model achieves the 99% accuracy and 90% recall initially
- **Continuous improvement:** constinuously refine and improve the model to be used based on new data collected after its implementation.
- **Feature-driven fraud prevention:** the explanation of the model suggest that the transaction amount and hour of transaction might be particularly important when is comes to fraud. The company should investigate further if it is worth to take some fraud prevention action based on these features (e.g., adding extra verification for transactions over a certain amount or between 22h00 and 03h00)

For an visual presentation of the project, visit: https://github.com/diogofn1/Fraud-detection/blob/main/Machine%20Learning%20Project%20-%20Presentation.pdf.
