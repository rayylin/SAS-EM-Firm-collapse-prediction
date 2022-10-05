# SAS-EM-Firm-collapse-prediction
Firm collapse prediction has been a subject of interest for almost a century and it still ranks high among the hottest topics in economics. The aim of predicting financial distress is to develop a predictive model that combines various econometric measures and allows one to foresee a financial condition of a firm. The purpose of bankruptcy prediction is to assess the financial condition of a company and its future perspectives within the context of longterm operation on the market.


    The raw data for training set contains 64 predictors and 1 target variable
    Columns
    attr1 - net profit / total assets
    attr2 - total liabilities / total assets
    attr3 - working capital / total assets
    attr4 - current assets / short-term liabilities
    attr5 - [(cash + short-term securities + receivables - short-term liabilities) / (operating expenses - depreciation)] * 365
    attr6 - retained earnings / total assets
    attr7 - EBIT / total assets
    attr8 - book value of equity / total liabilities
    attr9 - sales / total assets
    attr10 - equity / total assets
    ...
    
# Steps to make a prediction
1. EDA
2. Data Partitioning
3. Dealing with missing value and outliers
4. Modeling
6. Evaluation

# Try different preprocessing and modeling methods
Make sure that always do data partition before any preprocessing, because testing set should never be touched or changed.
We tried preprocessing methods, such as replacement, re
    
# Different combinations and ensembing 
![image](https://user-images.githubusercontent.com/58899897/194169959-4bd8a932-4cee-4b52-a324-6e0e91c89edd.png)
