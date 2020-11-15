# Overview
The objective of this repository is to study the dataset IBM HR Analytics Employee Attrition and Performance dataset. The project includes 2 parts: data exploratory analysis and building predictive models for attrition rate. 

## PART 1 - DATA EXPLORATORY ANALYSIS


### Objective

The objective of this part is to discover the reasons why employees quit at IBM. Questions in concerned can be: 
- What affects their decision to leave?  
- At what age are they more likely to leave?  
- Are they happy with the working environment?  
- What is the average amount of years employees tend to stay until they decide to leave?  

### Types of Analysis

There are 4 parts in Exploratory Data Analysis:
- Data information 
- Univariate Analysis
- Bivariate Analysis
- Multiple Correspondence Analysis

<img src="https://github.com/huongdo108/employee-attrition-analysis/blob/master/images/mca.png" align="centre">

The variables that explain the variances the most are 'JobLevel','JobRole', 'MonthlyIncome', 'TotalWorkingYears', 'YearsAtCompany', 'YearsInCurrentRole', 'YearsWithCurrManager'.

Employees who have the highest likelihood to leave are young, have low income, low job level, and few year working experiences (less than 6 years). On the contrary, employees who are more likely to stay have high income, high job level and position, many years of working experiences. Human resource employees are more likely to leave than technician and research employees.

Overall, it can be concluded that leaving employees are more likely not happy with their current work environment, situation, the job itself as well as salary or they are still young and want to experience more.

## PART 2 - DATA MODELLING

### Objective

The objective of this notebook is to build predictive models to predict employee attrition rate for Kaggle's dataset, IBM HR Analytics Employee Attrition and Performance.

### Modelling

**Features engineering**

<img src="https://github.com/huongdo108/employee-attrition-analysis/blob/master/images/feature_engineer.PNG" align="centre">

**Classification model**

    - Logistic Regression
    - Random Forest Classifier
    - Gradient Boosting Classifier

**Model evaluation**

<img src="https://github.com/huongdo108/employee-attrition-analysis/blob/master/images/performance.PNG" align="centre">

**Model optimization**
- Goal: Improve recall score to classify as many quitting employees as possible, while the cost of classifying quitting employees as non-quitting is higher than the cost of classifying non-quitting employees as quitting is assumed.
- Methods:
    - Random Search: Search for the best parameters of three models to improve the recall score.
    - Factor Analysis: Implement the best parameters found by Random Search into three models. Feed each model with different numbers of component analysis to observe how the recall and precision scores fluctuate.
    - Best Features Selection: Implement best parameters from Random Search into three models. Feed each model with different numbers of best features produced by each model to observe how the recall and precision scores fluctuate.
- Performance: 
    - Recall and precision scores remain constant in Logistic Regression while fluctuate drastically in Random Forest and Gradient Boosting classifiers.
    - The overall obtained maximum recall score is approximately 71%. Thus, there is some small improvement from the original results in slide 12.


<img src="https://github.com/huongdo108/employee-attrition-analysis/blob/master/images/model_optimization.PNG" align="centre">


**Model comparision**

<img src="https://github.com/huongdo108/employee-attrition-analysis/blob/master/images/model_optimization_recall.PNG" align="centre">

**Most important features**

<img src="https://github.com/huongdo108/employee-attrition-analysis/blob/master/images/feature_importance.PNG" align="centre">