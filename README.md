# credit-risk-classification
Report analysis:
The purpose of this analysis is to predict the loan status. The dataset includes various variables that can be used to make predictions. To evaluate the accuracy of predicting the loan status, we will apply logistic regression, splitting the data into feature variables (X) and target labels (y).
* Explain what financial information the data was on and what you needed to predict.
The dataset provided information on lending, with the following columns: loan_size, interest_rate, borrower_income, debt_to_income, number_of_accounts, derogatory_marks, and total_debt. These columns, excluding loan_status, were used as the feature variables (X), while loan_status served as the target label (y). The goal of the analysis was to predict the loan_status to classify loans into two categories: 'healthy loan' (0) and 'high-risk loan' (1) and determine their respective quantities or percentages.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
The variable I aimed to predict was loan_status, which has two possible outcomes: healthy_loan (0) and high_risk_loan (1). A healthy_loan indicates that the loan is in good standing, with no past-due payments or other issues with repayment. In contrast, a high_risk_loan indicates that there have been issues, such as missed payments or overdue amounts. Predicting this status can help identify potential issues early, allowing for timely intervention before problems with repayment arise.
* Describe the stages of the machine learning process you went through as part of this analysis.
I followed the typical stages of the machine learning process in this analysis. First, I explored the dataset and defined the problem to predict the loan status (healthy or high-risk) based on financial features. I then processed the data by cleaning it, handling missing values, and splitting it into two categories: variables (X) and labels (y). After preprocessing, I used logistic regression as the classification model because it is suitable for binary outcomes. I trained the model on the data, allowing it to learn the relationship between the input features and the loan status. The model’s performance was evaluated using precision, with a 99% precision for predicting healthy loans, which was very satisfying, and an 85% precision for high-risk loans, which was considered acceptable. Overall, the logistic regression model performed well in classifying loan status.
--Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model:
    * Description of Model  Accuracy, Precision, and Recall scores.
      
Classification Report
                                        precision    recall  f1-score   support

           0                             1.00         0.99      1.00        18765
           1                             0.85         0.91      0.88          619

    accuracy                                                    0.99         19384
   macro avg                             0.92         0.95      0.94         19384
weighted avg                             0.99         0.99      0.99         19384

To summarize, the results from the table show that the prediction for '0' (healthy loans) was highly accurate, with a precision of 1.00. For '1' (high-risk loans), 85% of the predictions were correct. The recall indicates that with a score of 0.99, the logistic regression model correctly identifies 99% of actual healthy loans. However, the recall is 91% for high-risk loans, meaning the model only identifies 91% of actual high-risk loans. Overall, based on other metrics such as accuracy, F1 score, macro average, and weighted average, we can conclude that the healthy loans (0) prediction was very good. In contrast, for high-risk loans (1), the performance was acceptable but not as strong. Having more accurate predictions for high-risk loans is important since inaccurate predictions could lead to issues with loans not being paid on time. Despite this, I would still recommend using this model because its overall performance is satisfactory, especially for healthy loans. However, improving the prediction accuracy for high-risk loans could be a priority for future model refinement.
