# Developers-Hub-AI_ML-Internship_Tasks
Machine learning, data preprocessing, visualization, and model development tasks completed during the Developers Hub AI/ML Internship.
---
# Task 1: Exploring and Visualizing a Simple Dataset
## Objective:
Learn how to load, inspect, and visualize a dataset to understand data trends and distributions.
## Dataset Used:
Iris Dataset
## Total Samples:
150
## Features:
* sepal_length
* sepal_width
* petal_length
* petal_width
* species
## Libraries Used
* pandas
* matplotlib
* seaborn
## Platform / Environment
* Google Colab
## Tasks Performed
* Loaded the dataset using pandas
* Inspected dataset shape and column names
* Displayed first 10 rows using .head(10)
* Used .info() and .describe() for statistical analysis
* Checked missing/null values
* Created scatter plots and pairplot to analyze feature relationships
* Created histograms to visualize feature distributions
* Created box plots to identify outliers
## Visualizations
### Scatter Plots
Created two scatter plots to analyze relationships between features:
* Sepal Length vs Sepal Width
* Petal Length vs Petal Width
A pairplot was also created to visualize relationships between all feature combinations grouped by species.
### Histograms
Histograms were used to visualize the value distributions of all numerical features and observe how the data is spread across different ranges.
### Box Plots
Box plots were used to identify outliers and visualize the spread of numerical features.
## Key Observations
* Petal length and petal width are highly discriminative features.
* Setosa species is clearly separable from the other species.
* Versicolor and Virginica show slight overlap in scatter plots.
* Sepal length and sepal width show moderate correlation.
* Sepal width contains some outliers visible in the box plot.
* Sepal width shows a relatively symmetric distribution.
* Petal length and petal width show multimodal distributions due to differences between Iris species.
* Histograms help visualize the spread and concentration of feature values.
* No missing/null values were found in the dataset.

## Task File
* [Open Task 1 Notebook](./DHC_Task_1.ipynb)


# Task 2: Predict Future Stock Prices

## Objective:

Use historical stock market data to predict the next day's closing stock price using regression models.

## Dataset Used:

Amazon Stock Market Data (Yahoo Finance)

## Stock Selected:

Amazon (AMZN)

## Dataset Source:

Yahoo Finance API using the `yfinance` Python library

## Features Used:

* Open
* High
* Low
* Volume

## Target Variable:

* Next_Close (Next Day Closing Price)

## Libraries Used

* yfinance
* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn

## Platform / Environment

* Google Colab

## Tasks Performed

* Retrieved historical Amazon stock data using `yfinance`
* Inspected dataset using `.head()`, `.shape`, `.info()`, and `.describe()`
* Checked duplicate values using `.duplicated().sum()`
* Checked missing/null values using `.isnull().sum()`
* Visualized stock closing price trends using Seaborn line plots
* Performed feature engineering by creating the `Next_Close` target column
* Split the dataset into 80% training and 20% testing sets
* Applied StandardScaler for feature standardization
* Trained a Linear Regression model
* Predicted next-day stock closing prices
* Evaluated model performance using regression metrics
* Visualized actual vs predicted stock prices using line plots

## Visualizations

### Line Plot

A Seaborn line plot was created to visualize Amazon’s closing stock prices over time and observe overall market trends.

### Actual vs Predicted Plot

A comparison line plot was created to compare actual stock prices with predicted stock prices.

## Regression Metrics Used

### Mean Absolute Error (MAE)

Measures the average absolute prediction error.

### Mean Squared Error (MSE)

Measures the average squared prediction error.

### Root Mean Squared Error (RMSE)

Measures prediction error in the same unit as stock prices.

### R² Score

Measures how well the regression model explains the variance in stock prices.

## Model Used

### Linear Regression

Linear Regression is a supervised machine learning algorithm used for predicting continuous numerical values by learning relationships between input features and the target variable.

## Key Observations

* Amazon stock prices showed an overall increasing trend over time.
* Open, High, and Low prices showed strong positive correlation with closing prices.
* No duplicate values were found in the dataset.
* No major missing/null values were present after preprocessing.
* The Linear Regression model achieved strong predictive performance.
* Low MAE and RMSE values indicated small prediction errors.
* The R² score was approximately 0.99, indicating excellent model performance.
* Actual and predicted stock price lines were closely aligned, showing accurate predictions.

## Task Files
* [Open Task 1 Notebook](./DHC_Task_2.ipynb)



