# Customer Complaints Analysis

This project aims to predict customer complaints based on transaction history data. The goal is to identify customers who are more likely to complain and proactively address their concerns, ultimately reducing the number of complaints and improving overall customer satisfaction.

## Problem Statement

Customers of our store have been complaining regularly on social media posts. To address this issue, we have decided to start a campaign to call customers who are more likely to complain. The objective is to collect their opinions and feedback on how we can serve them better. Using the transaction history data from the last 30 days, we need to develop a machine learning model to predict whether a customer will complain by the end of the month or not.

## Approach

The project follows the following approach:

1. **Exploratory Data Analysis (EDA)**: Performed exploratory data analysis to understand the transactional data, identify patterns, and gain insights into customer behavior and complaint trends. All visualizations are saved in `../EDA_plots` directory for further reference and presentation.

2. **Data Preprocessing**: Handle missing values, perform feature engineering, and encode categorical variables to prepare the data for model training.

3. **Feature Engineering & Feature Selection**: Utilizing datetime features and other historical informations to generate new features which are more insightiful and powerful in uncovering pattern to predict lilehood of customer to complain. Selected relevant features based on their significance in predicting customer complaints. Use Insights from Analysis, and domain knowledge to identify the most important features.

4. **Model Training**: Trained a machine learning model using the 80% of labeled data to predict the likelihood of customer complaints. Evaluate multiple models such as Logistic Regression, Random Forest, LightGBM, and CatBoost to identify the best-performing model.
Catboost and Random Forest outshed other models with their default parameters. I opt to move forward with Random Forest Model based on the goal and risks.

5. **Model Evaluation**: 20% of the labeled data used in assesment of the model performance. I considered accuracy, F1-Score, AUC and Confusion Matrix in assess the quality and predictive power of Random Forest Classifier on customer complaints accurately.

6. **Feature Importances**: Analyze the feature importances from the trained Random Forest model to understand which features contribute the most to identifying customers with complaints. Use this information to gain insights into customer behavior and make data-driven decisions.

7. **Model Explainability**: Utilized LIME to uncover the prediction of Random Forest Classifier per each instance(Local Explainability). This provide more insights, trust on the factors/variables contribution per results.


## Results

The Random Forest Classifier model outperformed other models with an accuracy of 82%, F1-score of 85%, and AUC of 82%. The confusion matrix for the model is as follows:

```
[[1831  738]
 [ 379 3437]]
```

The AUC score of 0.876 indicates that the model has good discriminatory power in distinguishing between customers who will complain and those who will not.

## Conclusion

Based on the analysis and model results, we can draw the following conclusions:

- The Random Forest Classifiers model trained on transaction history data can accurately predict whether a customer is likely to complain.
- Features such as balance on the complaint date, transaction amount, customer age, and product discounts have a significant impact on identifying customers with complaints.
- The call campaign can be targeted towards customers with a higher likelihood of complaining, as determined by the model predictions.
- Regular monitoring and evaluation of the campaign, along with continuous model updates, will help in improving customer satisfaction and reducing the number of complaints.

## Recommendations

Based on the findings of this project, the following recommendations are suggested:

1. Improve data collection: Consider collecting more detailed and comprehensive data related to customer transactions, interactions, and feedback. This additional data can provide deeper insights into customer behavior and preferences, enabling more accurate predictions and targeted campaigns.

2. Feature Scaling & Explore additional features: Normalising the range of features because are varying in degrees of magnitude, range and units. Experiment with generating new features based on the existing data to capture more information about customer behavior and preferences.

3. Incorporate external data sources: Look for relevant external data sources that can complement the existing transaction history. This may include demographic data, social media sentiment analysis, or customer satisfaction surveys. Integrating such data can provide a more comprehensive view of customer preferences and help identify potential areas for improvement.

4. Regular model retraining: Customer behavior and preferences can evolve over time, so it is important to regularly update and retrain the predictive model. Set up a system to periodically retrain the model using the latest transaction data to ensure it stays accurate and up to date.

5. Collaborate with customer service: Establish a strong feedback loop with the customer service team to gather insights from direct customer interactions. Regularly communicate the findings and recommendations from the predictive model to customer service representatives, enabling them to provide better support and tailored solutions to customers.

6. Continuously monitor and evaluate: Implement a system to track the performance of the call campaign and customer satisfaction metrics over time. Regularly monitor the impact of the campaign and make necessary adjustments to improve its effectiveness.

However, these recommendations can enhance our customer complaint management strategy and further reduce the number of complaints. This will not only result in improved customer satisfaction but also help build a positive brand reputation and foster long-term customer loyalty.
