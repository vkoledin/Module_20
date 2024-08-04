Overview of Analysis

This is an analysis of dataset of historical lending activity from a peer-to-peer lending services company. I built a model that can identify the creditworthiness of borrowers.

The data was based on loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, total debt and loan status and the prediction was based on the loan status. The variable is an int64. The analysis started with importing dependencies, importing the lending data, and separating the 'loan status' (y) column from the features(X). Data was split into test and train models using the train-test-split, with a random state of 1. Next, data was instantiated with the Logistic Regression model with a sag solver and random state of 1. Next, data was fitted with the train variables and predicted with the test variables. Lastly, the Confusion Matrix showed the number of correct and incorrect predictions for each class and the Classification Report provided precision, recall, F1 score, and support for each class, helping to understand the model's performance.



Results

The Logistic Regression Mode used predicted and classifed the following the scores: * Accuracy score of 0.99, * Precision score for healthy loan = 1, high-risk loan = 0.85, * Recall scores for healthy loans = 0.99, high -risk loan = 0.91.

Summary

Healthy Loan: *Perfect Precision: Every loan classified as healthy is truly a healthy loan. There are no false positives. *Implication: The model is extremely reliable in predicting healthy loans, ensuring no high-risk loans are mistakenly classified as healthy. This minimizes the risk of default among loans classified as healthy.

High-Risk Loan: *Lower Precision: While a significant portion (85%) of the high-risk predictions are correct, there are some false positives (15%). *Implication: Some healthy loans are incorrectly flagged as high-risk. This might lead to unnecessary preventive measures or higher interest rates for those borrowers, potentially affecting customer satisfaction and business.

RECALL SCORES

Healthy Loan: *The model is almost perfect at identifying healthy loans, both in terms of not missing any (high recall) and not making any false predictions (perfect precision). *Implication: The risk of misclassifying a high-risk loan as healthy is virtually eliminated, making the model very trustworthy for identifying good loans.

High-Risk Loan: *The model does well in identifying high-risk loans but not perfectly. Some healthy loans are misclassified as high-risk (precision less than 1), and some high-risk loans are missed (recall less than 1). *Implication: While the model captures most high-risk loans, it also falsely flags some healthy loans. This could lead to a conservative approach in lending, where some borrowers might face higher scrutiny or interest rates unnecessarily.

ACCURACY SCORE *High Accuracy: A score of 0.99 indicates that the model is highly accurate, with only 1% of the instances being misclassified. *Performance: Generally, this suggests that the model performs very well on the lending dataset, which is based the Logistic Regression Model.