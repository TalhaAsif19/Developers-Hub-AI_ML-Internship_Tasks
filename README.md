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
* [Open Task 2 Notebook](./DHC_Task_2.ipynb)


# Task 4: General Health Query Chatbot (PromptEngineering Based)
## Objective
Create a chatbot that can answer general health-related questions using an LLM (LargeLanguage Model).

---

# Model Used

## Mistral-7B-Instruct-v0.1

**Source:** Hugging Face Transformers Library

**Task Type:**
- Text Generation
- Conversational AI

---

# Libraries Used
- transformers
- torch
- warnings

---

# Platform / Environment
- Google Colab
- Python

---

# Features Implemented
- User input-based conversational chatbot
- Prompt engineering for friendly medical responses
- Safety filtering for dangerous medical situations
- Emergency keyword detection
- Interactive chatbot loop
- Clean response formatting
- Exit option using `q`

---

# Prompt Engineering

A custom system prompt was used to guide the model behavior.

## System Prompt

```python
SYSTEM_PROMPT = """
You are a helpful medical assistant chatbot.
Act like a top 1% helpful medical assistant.
Give simple and friendly health information.

Rules:
- Do not diagnose diseases.
- Do not prescribe medicines.
- Do not give exact dosage or overdose limits.
- For medicine questions, do not simply say "yes".
- Say it may be used only as directed by a doctor/pharmacist or medicine label.
- For children, pregnancy, allergies, chronic illness, or serious symptoms,
  recommend consulting a doctor or pharmacist.
"""
```

---

# Safety Handling

The chatbot includes a safety filter that checks for dangerous or emergency-related keywords before sending the query to the model.

## Dangerous Keywords Used

```python
danger_keywords = [
    "chest pain",
    "difficulty breathing",
    "overdose",
    "suicide",
    "stroke"
]
```

If dangerous keywords are detected, the chatbot immediately returns an emergency warning message instead of generating a response from the model.

---

# Tasks Performed
- Loaded the Mistral-7B-Instruct model using Hugging Face pipeline
- Built a chatbot function for user interaction
- Applied prompt engineering for safe and friendly responses
- Implemented safety filtering using keyword matching
- Added conversational loop for continuous chatting
- Added quit functionality using `q`
- Cleaned chatbot outputs for better readability
- Tested the chatbot using multiple health-related questions

---

# Sample Questions Tested
- What causes a sore throat?
- Is paracetamol safe for children?
- What are common symptoms of dehydration?
- How can I treat a mild headache at home?
- What is the overdose limit for paracetamol?

---

# Example Outputs

## User Query

```text
What causes a sore throat?
```

## Chatbot Response

```text
A sore throat can be caused by various reasons such as cold and flu,
bacterial or viral infection, postnasal drip, or irritation from smoking,
alcohol, or acidic foods. It is important to consult a doctor if symptoms
persist or worsen, or if you experience fever, severe pain, or difficulty swallowing.
```

---

## User Query

```text
Is paracetamol safe for children?
```

## Chatbot Response

```text
It may be used in children as directed by a doctor or pharmacist.
However, always consult a doctor or pharmacist before giving any medication to a child.
```

---

## User Query

```text
What are common symptoms of dehydration?
```

## Chatbot Response

```text
Common symptoms of dehydration include thirst, dry mouth, dark urine,
fatigue, headache, dizziness, and constipation. These symptoms may occur
more frequently in hot weather or during physical activity. It is important
to stay hydrated by drinking enough water.
```

---

## User Query

```text
What is the overdose limit for paracetamol?
```

## Chatbot Response

```text
This may be a serious medical emergency.
Please contact a doctor or emergency service immediately.
```

---

# Code Highlights

## Model Loading

```python
chatbot = pipeline(
    "text-generation",
    model="mistralai/Mistral-7B-Instruct-v0.1",
    pad_token_id=2
)
```

---

## Chatbot Function

```python
def health_chatbot(user_query):

    if safety_filter(user_query):
        return "This may be serious. Please contact a doctor or emergency service immediately."

    prompt = SYSTEM_PROMPT + "\nUser: " + user_query + "\nAssistant:"

    response = chatbot(
        prompt,
        max_new_tokens=300,
        temperature=0.5,
        do_sample=True,
        return_full_text=False
    )

    answer = response[0]["generated_text"].strip()

    return answer
```

---

# Skills Learned
- Prompt Engineering
- Conversational AI Development
- Hugging Face Transformers
- Large Language Model Integration
- Safety Handling in AI Chatbots
- Python-based Chatbot Development

---

# Note About GitHub Notebook Preview

The original notebook contained interactive chatbot runtime outputs generated during testing in Google Colab.

To ensure proper rendering and compatibility on GitHub, output cells were cleared before uploading because GitHub sometimes fails to render notebooks containing large interactive outputs or widget metadata from LLM/chatbot sessions.

The chatbot was fully tested successfully in Google Colab, and the sample chatbot questions and responses are provided above in the README file for reference.

---

# Conclusion
This task successfully demonstrates the development of a simple health assistant chatbot using a pre-trained Large Language Model. Prompt engineering and safety filtering were applied to ensure that the chatbot provides user-friendly and safer health-related information while avoiding harmful medical guidance.

## Task Files
* [Open Task 4 Notebook](./dhc_task_4.ipynb)
