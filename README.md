# credit-risk-classification

In this project, we applied machine learning techniques to evaluate a dataset containing historical lending activities of a peer-to-peer lending services company. Our main objective was to develop a model capable of accurately categorizing the creditworthiness of borrowers.

Overview of the Analysis
The analysis encompassed various factors, including:

Loan amount
Interest rate
Borrower's income
Debt-to-income ratio
Number of accounts held by the borrower
Derogatory marks against the borrower
Total debt
The dataset comprised 77,536 data points, which we divided into training and testing sets. We initially used the training set to construct a logistic regression model, labeled as Logistic Regression Model 1, utilizing the LogisticRegression module from scikit-learn. Subsequently, we applied Logistic Regression Model 1 to the testing dataset to evaluate its performance in classifying loans as either low-risk or high-risk.

The initial model was trained on a dataset consisting of 75,036 low-risk loan data points and 2,500 high-risk data points. To address the class imbalance and ensure equal representation in the training data, we employed the RandomOverSampler module from imbalanced-learn. This resampling technique generated 56,277 data points for both low-risk (0) and high-risk (1) loans while preserving the essential characteristics of the original dataset.

We then used the resampled data to construct a new logistic regression model, referred to as Logistic Regression Model 2. The primary objective of this model remained unchanged—to classify loans in the testing set as either low-risk or high-risk.

Results
Logistic Regression Model 1:

Precision: 93% (averaged; 100% precision for low-risk loans, 87% for high-risk loans)
Accuracy: 94%
Recall: 95% (averaged; 100% recall for low-risk loans, 89% for high-risk loans)
Logistic Regression Model 2:

Precision: 93% (averaged; 100% precision for low-risk loans, 87% for high-risk loans)
Accuracy: 100%
Recall: 100%
Summary
Logistic Regression Model 2 demonstrates a decreased likelihood of producing false negatives, enhancing its reliability in identifying high-risk loans. It is worth noting that Logistic Regression Model 2 predicts slightly more false positives (misclassifying low-risk loans as high-risk). If the primary objective is to evaluate the likelihood of high-risk loans, neither model achieves precision exceeding 90%. Nonetheless, Logistic Regression Model 2 outperforms the initial model in terms of accuracy and recall, making it the preferred choice due to its high overall accuracy and recall rates
