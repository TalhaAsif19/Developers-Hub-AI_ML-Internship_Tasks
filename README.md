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

## Task Files
* [Open Task 1 Notebook](./DHC_Task_1.ipynb)

