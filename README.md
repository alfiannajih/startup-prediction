# Startup Success/Fail Prediction
This is my personal project, the motivation of this project is to gain some knowledge about Exploratory Data Analysisi (EDA) and data preprocessing. The source of the datasets come from [kaggle datasets](https://www.kaggle.com/datasets/yanmaksi/big-startup-secsees-fail-dataset-from-crunchbase)
<br>
The scope of this project:
1. Exploratory Data Analysis
2. Data Preprocessing
3. Modeling
4. Tune in Hyperparameter
5. Evaluation on Test Data

There are two notebooks in this project, first with base assumptions and second with additional assumptions:
1. Base Assumptions
    - We assume the minimum funding total is 1000 usd.
    - We impute categorial_list with 'Others' value.
2. Additional Assumptions
    - Same as base assumptions.
    - We drop some duplicated startup based on another columns (ignoring the permalink uniqueness).
    - Logically datetime should be founded_at < first_funding_at < last_funding_at, so anything that not in this order we will convert it to *None*.
    - We set threshold for category_list count, if it less than threshold we will impute 'Others' value.

## 1. Exploratory Data Analysis
In this section, we will inspect our data with these following steps:
- Data that we will used in data preprocessing.
- Check how many *None* values data that we will impute in data preprocessing.
- Check the validity of the data types.
- Check the distribution of the data.
- Find the outliers

## 2. Data Preprocessing
In this section, we will build our pipeline to transform our data so it is become a valid input for our machine learning model.

## 3. Modeling
We will build our baseline model by using Dummy model from sklearn based on most_frequent and randomness strategy. After that, we will train our model by using logistic regression, random forests, gradient boosting, and neural network. Then we will compare our result with baseline model.

## 4. Tune in Hyperparameter
We will choose two model from previous section and then tune in hyperparameters in order to improve our accuracy.

## 5. Evaluation on Test Data
Finally, we will evaluate those two model with our test data and compare it, then we will choose the best model from that evaluation.