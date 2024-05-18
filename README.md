# Fraud Classifier

This project aims to tackle the escalating challenge of credit card fraud detection using machine learning algorithms. We focus on employing two primary models, XGBoost and SVM, to classify fraudulent transactions within a credit card transaction dataset sourced from Kaggle.

## Abstract

Using the Kaggle credit card transaction dataset, I developed a fraud detection classifier where the XGBoost model demonstrated superior performance over SVM in terms of AUC, interpretability, computational efficiency, and robustness. The models were trained with particular attention to addressing the imbalanced nature of the fraud classification problem using techniques such as SMOTE.

## Data

The dataset comprises transactions with features such as distance from home, transaction distance from last transaction, and whether the transaction was made using a chip, among others. It includes both continuous and discrete variables, detailed in the `Data Description` section below.

### Data Description

- **distance_from_home**: Continuous. Distance from home where the transaction occurred.
- **distance_from_last_transaction**: Continuous. Distance from the last transaction.
- **ratio_to_median_purchase_price**: Continuous. Ratio of the transaction price to the median purchase price.
- **repeat_retailer**: Discrete. Whether the transaction was at the same retailer.
- **used_chip**: Discrete. Whether the transaction was made using a chip.
- **used_pin_number**: Discrete. Whether a PIN was used in the transaction.
- **online_order**: Discrete. Whether the transaction was an online order.
- **fraud**: Discrete. Whether the transaction was fraudulent.

## Models

### XGBoost Model

- Trained using the `xgb.train()` function in R, with parameters optimized to prevent overfitting.
- Achieved an AUC of 0.9891.

### SVM Model

- Utilized a Support Vector Machine with a radial kernel.
- Data was normalized to enhance performance given SVM's sensitivity to feature scaling.
- Achieved an AUC of 0.8723.

