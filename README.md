# Heart Attack Risk Analysis

>School of Computer Science and Computer Engineering \
Nanyang Technological University \
Lab Group: FCS7 \
Team 10


## Our Team
| Name | Github ID |
|---|---|
| Harikrishnan Vinod | [@harikrishnanvinod](https://github.com/harikrishnan-vinod) |
| Lim En Jia | [@enjiaaaa](https://github.com/enjiaaaa) |
| Muhammad Hanif | [@HanifRendevu](https://github.com/HanifRendevu) |

## Source of Dataset
The [dataset](https://www.kaggle.com/datasets/iamsouravbanerjee/heart-attack-prediction-dataset/data) is from Kaggle, by Sourav Banerjee, titled "Heart Attack Risk Prediction Dataset".

## Context
According to the World Health Organisation, cardiovascular disease is the leading cause of death globally, taking an estimated 17.9 million lives yearly, 32% of global deaths, and 85% were due to heart attacks.
In Singapore, it is reported 11631 heart attack cases per 100k people (7,344 in 2010), averaging 31 a day. Among them, 9.2% died within 30 days.

Up to 80% of premature heart attacks can be prevented with risk management.


## Problem Statement
To find out how different factors affect the risk of heart attack among individuals.

## Our Goal
To leverage **machine learning** to accurately assess the risk of heart attacks for individuals using the different factors from the dataset


## Data
The following is the factors we will be looking at

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/20bdfa97-275f-4b1a-acae-7ac35b32b274" width="400">

## Data Cleaning
### 1. Blood pressure data consists of both systolic blood pressure level and diastolic blood pressure level separated by a /.

We initialise 2 new variables `Systolic_Blood_Pressure` and `Diastolic_Blood_Pressure`.

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/bf3ea47f-fecd-4fd8-85c7-99fe8cf41bcb" width="600">

### 2. Dropped 4 factors
   - `Patient ID` : irrelevant
   - `Country` & `Hemisphere` : Are better represented by continent to show distribution of the participations
   - `Blood Pressure` : Split into Systolic and Diastolic Blood Pressure earlier

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/f547c892-d01f-408f-8873-f6628e0ea258" width ="600">

### 3. Remove Outliers
   - It helps to improve the performance of the model
     
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/f20cac37-4677-45fe-8f58-9beaf7397aae" width="600">
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/6da3ae39-608c-4b12-b170-435404959b1d" width="600">

### 4. Ensure that our data is non-null
   - It ensures data integrity

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/34903d89-281d-4478-831f-b90fb56a0ef1" width="150">

## Categorising Variables into 4 Categories
   - This helps when trying to capture non-linear relationships between variables and the target variable like in this case.
     
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/a4c98fac-a3a1-43fd-9498-1084f1ea7ab5" width="600">

## Heat Maps that show Correlation
   - This shows which variables are related to the risk of having Heart Attack
     
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/5a7eb960-c5e1-4e10-9bf9-a16d56427454" width ="600">
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/cf63576d-b093-48c4-8181-4a3e611c0b9a" width ="600">


## Variables Chosen from Each Category
   - From each category, we picked the variable with the highest correlation to Heart Attack Risk to be used in our Machine Learning Model to predict Heart Attack Risk
     
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/153801ad-e569-4f31-a208-9fe2ddf0651f" width="600">

## Exploratory Data Analysis
### 1. Income Level
People with **higher** Income Level tend to have a **lower** Heart Attack Risk

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/542909d0-089d-45aa-971a-2b38ee0facbb" width="600">

### 2. Systolic Blood Pressure
**Higher** Systolic Blood Pressure points to a **higher** Heart Attack Risk

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/6fc03755-50ed-4f51-b2a3-80f40db63890" width="600">

### 3. Cholesterol
**Higher** cholesterol levels tend to lead to a **higher** Heart Attack Risk

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/0dfdc227-a1e5-4a8a-bdbb-258310b1ed79" width="600">

### 4. Medication Use
Despite having the highest correlation value under Medical History sub-categorical group, Medication Use **does not affect** Heart Attack Risk

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/0224b965-a5c4-4899-955a-b08e67942957" width="600">


## Our Mission
To accurately classify the Heart Attack Risk (0 or 1) of an individual based on these factors using Machine Learning 

## Machine Learning Models
We decided to use these 4 machine learning models to be able to predict Heart Attack Risk based on the factors of `Income` , `Systolic Blood Pressure` , `Cholesterol` and `Medication Use` which are our predictor variables. We did that by first splitting the train and test data randomly in a **70/30** split respectively and then using these models to learn from our train data and to see if it would be able to accurately predict our test data.
   
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/980361b3-e2e8-44aa-aae3-b40abdb0fcc8" width ="600">

## 1.Linear Regression
`Linear Regression` is a **machine learning model** that describes the relationship between a dependent variable, y, which in this case is the Heart Attack Risk, and one or more independent variables, x, which are our chosen variables. The goal is to find the **best-fitting linear line** that **minimises the sum of squared differences** between the observed and predicted values.
 The line is described by the equation:
   - 𝑦 =𝑚𝑥+c

### Univariate Linear Regression
#### **Income:**

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/ecbd224d-d744-4cca-a75d-a41a5aa2ae93" width = 600>

#### **Systolic Blood Pressure:**

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/f83e6ed2-5423-4002-b494-bac6c70ccb06" width = 600>


#### **Cholesterol:**

<img src ="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/648b24ce-1206-40b2-b42f-bc161a840424" width = 600>

#### **Medication Use:**

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/5ab71cab-3f51-4c3d-a5a3-0f56af891b56" width = 600>

### Findings for Linear Regression
The **negative explained variance** told us that the Linear Regression model fits the data very badly. We found out that the linear regression model is **not an accurate model** to represent Heart Attack Risk which takes on a **binary value** of 0 or 1. This is because Linear Regression assumes a linear relationship between the independent variables and the dependent variable and as such is unable to capture the **non-linear relationships** between predictor variables and the binary outcome. 


## 2.Logistic Regression
`Logistic Regression Model` in which a **logistic function** is used to model the relationships between predictor variables and the binary response variable. The model estimates the coefficients of the model that maximises the probability of the observed data
   ### UniVariate Lgositic Regression
   #### **Income:**
   **Test Accuracy: 0.6435907189045265**

   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/ac40ce6d-576b-4f3e-b9c3-5863447cbad7" width="600"> 

   #### **Systolic Blood Pressure:**
   **Test Accuracy: 0.6451122099657665**

   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/25436725-2929-4ce8-99eb-91182c57a824" width="600">

   #### **Cholesterol:**
   **Test Accuracy: 0.6496766831494865**

   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/38cf1057-3f15-4713-ae53-8785051a380c" width="600">

   #### **Medication Use:**
   **Test Accuracy: 0.6356028908330164**

   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/3ff7d8a0-c210-4da4-87bd-e100663460de" width="600">

   ### Multi-Variate Logistic Regression
   `Multivariate Logistic Regressions` enables us to capture **more complex relationships and interactions among variables that may not be apparent when considering only one predictor variable at a time.**
   We then proceeded to do a `Multivariate Logistic Regression Model` where all the predictor variables were used together to predict Heart Attack Risk.

   ![image](https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/80133350-c989-4517-a620-acd4f98d5ea5)

## 3. Random Forest Machine Learning
`Random Forest` is similar to a group decision-making team in machine learning. It combines the opinions of many “ decision trees”. It then takes these many decision trees and combines them to **avoid overfitting** which would then produce more accurate predictions. We included it because it can handle noisy data and is efficient with large datasets. It is a method that has been successfully used in many different fields of research and is definitely a popular ML algorithm in health care.
   ## First Iteration:
    In our first iteration, the model returned a low accuracy with very high False Negative Rate.

   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/54e32ec0-a73f-453e-b5a7-ca9226b68498" width="600"> 
   
   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/cbb77a43-2a37-413c-b029-20803294f937" width="600">

   We sought to improve upon this model to be able to better predict the Heart Attack Risk.
   
   ### Second Iteration:
   In our second iteration of the Random Forest model, we increased the max_depth to 20 and the number of estimators to 2000.
   -> n_estimators = 2000 and max_depth = 20

   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/ad142791-ad34-45c5-8be9-fda84cc7f73f" width =600>

   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/709a8a8a-0ab5-4178-944d-5e5be3929956" width =600>

   This model although had a higher accuracy, had an even higher False Negative Rate.

   ### Using GridSearch CV to find Best Model
   We attempted to use GridSearch CV to find the best Model for Random Forest.
   
   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/3a66b653-623a-4e03-bb5b-658484e3012f" width="600">
   
   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/13733577-5219-44af-9bb9-e4f5a6556234" width="600">
   
   Although this model had higher accuracy,we realized that the False Negative Rate is too undesirable as it classifies everything as having no Heart Attack Risk.

   ### Best Random Forest Iteration
   
   For our final model for Random Forest Machine Learning, we decided to adjust and balance the data when building the model.
   
   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/82f54208-15d4-4e0a-8a57-a6db36f08629" width="600">

   We attained our highest accuracy while also having a higher True Positive Rate and much Lower False Negative Rate.

## 4. K-Nearest Neighbour Machine Learning
K-Nearest Model is a supervised learning classifier that is non-parametric and distance based. Based on the fact that data points with similar characteristics usually belong in the same class, it tries to locate all nearest neighbouring data points to figure out the class that the particular data point belongs to.


Firstly, we standardise our data variables to ensure that all variables are of the same scale to prevent unnecessary domination.
   ### First Iteration

   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/ec6a6ae9-6d2c-45dc-859d-d5f2b1423b14" width =600>

   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/9eb95fb1-1993-42fa-95a5-af79aa3f83af" width =600>

   On our first run, we managed to obtain a model with an accuracy of 0.6071 but also a ridiculously high False Negative Rate.

   ### Improvements to the model
   We sought to fine tune this model by using a grid of hyperparameters for the KNN classifier, with the range of n being 1 to 60. The following graph shows the      grid of hyperparameters. We included cross validation to reduce bias as well as variance in model evaluation by splitting data into 5 folds. Search is done over the hyperparameter grid and the model is fit with different combinations of hyperparameters, with the cross-validation to assess performances.

   <img src ="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/7fb4e224-2030-4bbc-b14e-e3819e73115d)" width =600>

   ### Final Iteration

   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/118de2ca-b0d4-4421-b116-cf76c09fbda3" width =600>

   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/dfdca633-2745-4e59-a233-6658afe1fc9d" width =600>

   It returns a better test accuracy than the first model and a neighbour value of 46 but still has an extremely high False Positive Rate which is even higher than the first model.

## Conclusion
Out of the 4 machine learning models, Random Forest is the model that is best at predicting Heart attack risk among individuals, having the highest accuracy of 0.6930 and a F1-score of around 0.7.

However, these variables are not considered high enough. It shows that the current set of data and variables used are not able to accurately predict `Heart Attack Risk`. However, these are proven to be the variables from each category with the highest correlation to Heart Attack Risk. It reveals that the complexity of factors contributing to heart attack risk and the variables included in our analysis cannot fully capture it. As such, we believe that **further research incorporating advanced modelling techniques** and a broader range of variables may be necessary to gain deeper insights into the complex nature of heart attack risk and improve prediction accuracy.
For example BMI, is not an accurate representation of health and the diet stated in the data set is subjective. Medical test and proper medical advice from professionals would be a more accurate way to determine ones heart risk. Exploring additional variables, collecting more comprehensive datasets, or experimenting with different feature engineering techniques could potentially improve predictive performance.







   
   


   



