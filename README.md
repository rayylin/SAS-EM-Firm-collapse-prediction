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
    Used Graph Explore and Stat Explore to have a fundamental understanding of raw data.
    We could find that the data is highly biased, as most observasion would not go bankrupted.
    To solve that issue, we could use upsampling method.
2. Data Partitioning
    Train-Test Split 
    70% for training and 30% for testing
3. Data Preprocessing:dealing with missing value and outliers
    Replacement, Interactive Binning, Variable Transformation, etc.
    We found that the Replacement method performed well.
4. Modeling
    Neural Network, Random Forest, Decision Tree, Lasso, etc.
    After tuning each model, we could use different combinations and ensembling method.
5. Evaluation
    RSS, Misclassification rate, ROC, etc.
    
    


# Try different preprocessing and modeling methods
Make sure that always do data partition before any preprocessing, because testing set should never be touched or changed.
For each method, we also tried different parameters, evaluated the performance, and then created a model with parameters that perform better than default settings.

For example, we tried Neural Network with different number of hidden layers and nodes.
![image](https://user-images.githubusercontent.com/58899897/194190835-8f328d2a-9885-4ac9-b9db-f5b11e883496.png)

    
# Different combinations and ensembing 
![image](https://user-images.githubusercontent.com/58899897/194169959-4bd8a932-4cee-4b52-a324-6e0e91c89edd.png)
![image](https://user-images.githubusercontent.com/58899897/194190249-f819cc36-20b2-4d18-a63f-dbf87bbd9830.png)
![image](https://user-images.githubusercontent.com/58899897/194190279-96147599-0894-4e33-9b80-ea7bf7dd1719.png)


Model evaluation:
We used ROC and RSS to determine which model performed better.
We could not relied on only RSS, as it may have overfitting issue.

![image](https://user-images.githubusercontent.com/58899897/194190561-52f569a7-7798-4730-b93b-b2d4a7719d5c.png)


![image](https://user-images.githubusercontent.com/58899897/194190214-7debae66-418e-4567-9fe5-265dfd46273f.png)

![image](https://user-images.githubusercontent.com/58899897/194191317-f98a52ab-bfe6-43c3-848d-1449b698f106.png)

From the ROC curve we could see that model 1 (Green line) performed extremely well for the training set but not that well for the testing set
The ROC curve is created by plotting the true positive rate (TPR) against the false positive rate (FPR) at various threshold settings.
Final Result, we choose a model that performs well and has similar performance for both the training and testing set, as this result means that overfitting would not greatly affect our model.
