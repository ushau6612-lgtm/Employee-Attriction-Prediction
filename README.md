# Employee-Attriction-Prediction
Employee Attrition Prediction is a machine-learning project that predicts whether an employee is likely to leave a company.
# Employee Attrition Prediction

## Overview

Employee Attrition Prediction is a machine-learning project that predicts whether an employee is likely to leave a company based on various employee-related factors.

The project analyzes information such as salary, age, department, job role, working hours, years of experience, job satisfaction, overtime, distance from home, and years at the company.

A Logistic Regression model is used to perform binary classification and predict whether an employee is likely to stay or leave.

This project is intended for educational, academic, and machine-learning practice purposes.

## Objectives

* Analyze employee information.
* Understand employee attrition patterns.
* Identify factors associated with employee turnover.
* Clean and preprocess the dataset.
* Handle missing numerical and categorical values.
* Encode categorical variables.
* Standardize numerical features.
* Train a machine-learning classification model.
* Predict employee attrition.
* Calculate attrition probability.
* Evaluate model performance.
* Identify important factors related to attrition.
* Visualize employee attrition patterns.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Logistic Regression
* StandardScaler
* OneHotEncoder
* Pipeline
* ColumnTransformer

## Project Structure

```text
Employee_Attrition_Prediction/
│
├── employee_attrition.csv
├── employee_attrition_prediction.py
├── README.md
└── requirements.txt
```

## Dataset

The dataset contains synthetic employee information used to predict employee attrition.

### Dataset Features

| Feature                | Description                     |
| ---------------------- | ------------------------------- |
| employee_id            | Unique employee identifier      |
| age                    | Employee age                    |
| salary                 | Employee salary                 |
| department             | Employee's department           |
| job_role               | Employee's job role             |
| working_hours_per_week | Average weekly working hours    |
| years_of_experience    | Total professional experience   |
| job_satisfaction       | Employee job satisfaction score |
| overtime               | Overtime status                 |
| distance_from_home_km  | Distance from home to workplace |
| years_at_company       | Years spent at the company      |
| attrition              | Target variable                 |

## Target Variable

The `attrition` column represents the prediction target.

```text
0 = Employee Stayed
1 = Employee Left
```

## Data Preprocessing

The project uses a preprocessing pipeline to prepare the data for machine learning.

The following steps are performed:

1. Load the employee dataset using Pandas.
2. Display the first five records.
3. Check the dataset shape.
4. Check for missing values.
5. Remove `employee_id` because it is an identifier rather than a predictive feature.
6. Separate input features and the target variable.
7. Fill missing numerical values using the median.
8. Fill missing categorical values using the most frequent value.
9. Standardize numerical features using `StandardScaler`.
10. Convert categorical features into numerical representations using `OneHotEncoder`.
11. Split the dataset into training and testing data.

The dataset is divided into:

* 80% training data
* 20% testing data

Stratified splitting is used to maintain the distribution of attrition classes in the training and testing datasets.

## Machine Learning Algorithm

### Logistic Regression

The project uses Logistic Regression for binary classification.

The model predicts two possible outcomes:

```text
Employee Stayed
Employee Left
```

The Logistic Regression model is combined with the preprocessing pipeline using Scikit-learn's `Pipeline`.

This ensures that the same preprocessing steps are applied consistently during both training and prediction.

## Model Evaluation

The model is evaluated using several performance measures.

### Accuracy

Accuracy represents the percentage of predictions that are correctly classified.

### Classification Report

The classification report provides:

* Precision
* Recall
* F1-score
* Support

for employees who stayed and employees who left.

### Confusion Matrix

The confusion matrix provides information about:

* True positives
* True negatives
* False positives
* False negatives

This helps understand how well the model distinguishes between employees who stay and employees who leave.

## Example Employee Prediction

The project includes an example employee with the following information:

```text
Age: 28
Salary: 42000
Department: Sales
Job Role: Executive
Working Hours per Week: 55
Years of Experience: 5
Job Satisfaction: 2.0
Overtime: Yes
Distance from Home: 25 km
Years at Company: 2
```

The trained model predicts whether this employee is:

```text
Likely to Leave
```

or

```text
Likely to Stay
```

The program also calculates the probability that the employee will leave the company.

## Feature Importance

The project examines the coefficients of the Logistic Regression model to identify the factors most strongly associated with employee attrition.

The program displays the top 10 factors based on the absolute value of their model coefficients.

These factors can help understand which employee characteristics have a stronger relationship with the model's attrition predictions.

## Visualizations

The project generates two visualizations.

### 1. Attrition Rate by Department

A bar chart displays the percentage of employees who leave the company in each department.

The generated file is:

```text
attrition_by_department.png
```

### 2. Job Satisfaction and Working Hours

A scatter plot shows the relationship between:

* Job Satisfaction
* Working Hours per Week

The employee attrition outcome is also represented in the visualization.

The generated file is:

```text
satisfaction_vs_hours.png
```

## Installation

Make sure Python is installed on your computer.

Open a terminal in the project directory and install the required dependencies:

```bash
pip install -r requirements.txt
```

## Requirements

The project requires the following Python libraries:

```text
pandas
numpy
matplotlib
scikit-learn
```

## How to Run

After installing the dependencies, run:

```bash
python employee_attrition_prediction.py
```

The program will:

1. Load the employee dataset.
2. Display the first five rows.
3. Display the dataset shape.
4. Check for missing values.
5. Preprocess numerical and categorical features.
6. Split the dataset into training and testing sets.
7. Train the Logistic Regression model.
8. Generate predictions.
9. Calculate model accuracy.
10. Display the classification report.
11. Display the confusion matrix.
12. Predict the outcome for a sample employee.
13. Calculate the employee's attrition probability.
14. Display the top factors related to attrition.
15. Generate department-level attrition visualization.
16. Generate the satisfaction-versus-working-hours visualization.

## Output

The project produces:

* Dataset information
* Missing-value information
* Model accuracy
* Classification report
* Confusion matrix
* Employee attrition prediction
* Attrition probability
* Important model factors
* Department attrition visualization
* Job satisfaction and working hours visualization

The generated visualization files are:

```text
attrition_by_department.png
satisfaction_vs_hours.png
```

## Dataset Note

The included employee dataset is synthetic and is intended for educational and classroom machine-learning practice.

It does not contain real employee information.

## Disclaimer

The predictions generated by this project are intended for educational and analytical purposes only.

The model should not be used as the sole basis for employment decisions, employee evaluation, hiring, termination, promotion, or other workplace decisions.
