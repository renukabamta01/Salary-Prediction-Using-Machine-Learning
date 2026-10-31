# 💰 Salary Prediction Using Machine Learning


## 📌 Project Overview

Salary Prediction is a Machine Learning regression project that predicts an employee's estimated salary based on different professional and educational attributes.

The project uses historical salary data to identify patterns between employee characteristics and salary. It takes five input features — Job Title, Experience Years, Education Level, Industry, and Location — and predicts an estimated salary.

The project covers the complete Machine Learning workflow, including data exploration, preprocessing, feature selection, model training, evaluation, model serialization, and application development using Gradio.


## 🎯 Project Objectives

- Analyze salary-related data to understand employee characteristics.
- Perform Exploratory Data Analysis (EDA) to understand data distributions and patterns.
- Convert categorical features into numerical representations.
- Build and compare multiple regression models.
- Evaluate model performance using Root Mean Squared Error (RMSE).
- Develop an interactive application for salary prediction.


## 📂 Dataset Information

The dataset contains **250,000 records and 10 columns**.

| Column Name        | Description                          |
| ------------------ | ------------------------------------ |
| `job_title`        | Employee's job role                  |
| `experience_years` | Years of professional experience     |
| `education_level`  | Employee's educational qualification |
| `skills_count`     | Number of skills                     |
| `industry`         | Industry in which the employee works |
| `company_size`     | Size of the company                  |
| `location`         | Employee's geographical location     |
| `remote_work`      | Remote-work arrangement              |
| `certifications`   | Number of certifications             |
| `salary`           | Employee's salary (target variable)  |

**Selected Features:** Job Title, Experience Years, Education Level, Industry, and Location.

**Target Variable:** Salary.


## 🛠️ Technologies & Libraries Used

- **Python** – Programming language
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical operations
- **Matplotlib & Seaborn** – Data visualization
- **Scikit-learn** – Data preprocessing, model building and evaluation
- **Pickle** – Model serialization
- **Gradio** – Interactive application interface
- **Jupyter Notebook** – Development environment


## 🔄 Project Workflow


### 1. Data Loading and Understanding

- Loaded the dataset using Pandas.
- Explored dataset structure, dimensions, column names and data types.
- Used descriptive statistics to understand numerical features.


### 2. Exploratory Data Analysis (EDA)

- Checked for missing values and duplicate records.
- Analyzed numerical and categorical features.
- Examined experience, education and location distributions using visualizations.
- Identified patterns and understood the overall data distribution.


### 3. Data Preprocessing

- Applied Label Encoding to categorical features.
- Created separate encoders for Job Title, Education Level, Industry and Location.
- Converted categorical values into numerical representations.
- Selected five relevant input features for model training.


### 4. Feature Selection

Selected the following five features:

1. Job Title
2. Experience Years
3. Education Level
4. Industry
5. Location

The target variable was Salary.


### 5. Train-Test Split

Split the dataset into training and testing sets using Scikit-learn's `train_test_split()`.

- Training data: 80% (200,000 records)
- Testing data: 20% (50,000 records)
- Random state: 42


### 6. Model Building

Implemented and compared three regression algorithms:


**Linear Regression**

- A regression algorithm that models relationships between input features and a continuous target variable.


**K-Nearest Neighbors (KNN) Regressor**

- Predicts salary using the salary values of similar records in the training data.


**Decision Tree Regressor**

- Learns decision rules based on input features to predict a continuous numerical value.


### 7. Model Evaluation

Evaluated all three models using **Root Mean Squared Error (RMSE)**.

RMSE measures the difference between actual and predicted values. A lower RMSE indicates lower prediction error when comparing models on the same test set.


## 📊 Model Performance

| Algorithm               |      RMSE |
| ----------------------- | --------: |
| Linear Regression       | 30,877.18 |
| KNN Regressor           | 20,307.51 |
| Decision Tree Regressor | 22,590.45 |


**Best Performing Model:** KNN Regressor

KNN achieved the lowest RMSE among the three models in this experiment. Therefore, it was selected for the prediction application.


### 8. Model Saving

Used Python's Pickle library to serialize and save the trained KNN model in a `.pkl` file.

The saved model can be loaded later for making predictions without retraining it.


### 9. Application Development

Developed an interactive salary prediction interface using Gradio.

The application accepts the following inputs:

- Job Title
- Education Level
- Experience Years
- Industry
- Location

The input values are processed using the fitted encoders and passed to the trained model, which returns the estimated salary.


## 🚀 Application Features

- User-friendly Gradio interface.
- Text-based inputs for categorical features.
- Numerical input for experience years.
- Automatic categorical encoding.
- Real-time salary prediction after submitting inputs.
- Reusable trained machine learning model.
  

## 📚 Key Learnings

Through this project, I gained practical experience in:

- Understanding and exploring a large dataset.
- Performing EDA and data visualization.
- Handling categorical features using Label Encoding.
- Selecting input features and target variables.
- Understanding regression algorithms.
- Comparing machine learning models using RMSE.
- Saving and loading trained models using Pickle.
- Building an interactive application using Gradio.
- Understanding the end-to-end Machine Learning workflow
