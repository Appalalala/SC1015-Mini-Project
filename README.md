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

Up to 80% of premature heart attacks can be prevented with risk management


## Problem Statement
To find out how do the different factors affect the heart attack risk among individuals


## Data
The following is the factors we will be looking at

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/20bdfa97-275f-4b1a-acae-7ac35b32b274" width="600">

## Data Cleaning
1. Blood pressure data consists of both systolic blood pressure level and diastolic blood pressure level separated by a /.
We initialise 2 new variables Systolic_Blood_Pressure and Diastolic_Blood_Pressure.
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/bf3ea47f-fecd-4fd8-85c7-99fe8cf41bcb" width="600">

2. We drop these 4 factors
   - Patient ID : irrelevant
   - Country & Hemisphere : Are better represented by continent to show distribution of the participations
   - Blood Pressure : Split into Systolic and Diastolic Blood Pressure earlier

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/114349205/f547c892-d01f-408f-8873-f6628e0ea258" width ="600">

3. Remove Outliers
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/f20cac37-4677-45fe-8f58-9beaf7397aae" width="600">
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/6da3ae39-608c-4b12-b170-435404959b1d" width="600">

4. Ensure that our data is non-null

## Categorising Variables into 4 Categories 
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/a4c98fac-a3a1-43fd-9498-1084f1ea7ab5" width="600">

## Heat Maps to show Correlation
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/96a7423a-be66-40aa-944d-b3be972c59ff" width="600">
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/0d4ad86f-b1c9-4966-97f4-b9f1cf149420" width="600">

## Variables Chosen from Each Category
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/153801ad-e569-4f31-a208-9fe2ddf0651f" width="600">


### 1. Income Level
People with higher Income Level tend to have a lower Heart Attack Risk
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/542909d0-089d-45aa-971a-2b38ee0facbb" width="600">

### 2. Systolic Blood Pressure
Higher Systolic Blood Pressure points to a higher Heart Attack Risk
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/6fc03755-50ed-4f51-b2a3-80f40db63890" width="600">

### 3. Cholesterol
Higher cholesterol tends to lead to a higher Heart Attack Risk
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/0dfdc227-a1e5-4a8a-bdbb-258310b1ed79" width="600">

### 4. Medication Use
Despite having the highest correlation value under Medical History sub-categorical group, Medication Use does not affect Heart Attack Risk
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/0224b965-a5c4-4899-955a-b08e67942957" width="600">


## Our Mission
To accurately classify the Heart Attack Risk (0 or 1) of an individual based on these factors using Machine Learning 

## Machine Learning Models
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/980361b3-e2e8-44aa-aae3-b40abdb0fcc8" width ="600">

## 1.Linear Regression





## 2.Logistic Regression
Income:\
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/ac40ce6d-576b-4f3e-b9c3-5863447cbad7" width="600"> 

Systolic Blood Pressure:\
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/25436725-2929-4ce8-99eb-91182c57a824" width="600">

Cholesterol:\
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/38cf1057-3f15-4713-ae53-8785051a380c" width="600">

Medication Use:\
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/3ff7d8a0-c210-4da4-87bd-e100663460de" width="600">

## 3. Multi-Variate Logistic Regression
For Income, Systolic Blood Pressure, Cholesterol and Medication Use:
![image](https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/80133350-c989-4517-a620-acd4f98d5ea5)

## 4. Random Forest Machine Learning
   ## First Iteration: 
   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/54e32ec0-a73f-453e-b5a7-ca9226b68498" width="600"> 
   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/cbb77a43-2a37-413c-b029-20803294f937" width="600">
   ## Second Iteration:
   -> n_estimators = 2000 and max_depth = 20

   ## Using GridSearch CV to find Best Model
   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/3a66b653-623a-4e03-bb5b-658484e3012f" width="600">

   ## Trying with Best Model from GridSearch 
   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/13733577-5219-44af-9bb9-e4f5a6556234" width="600">
   
   ## We realized that the True and False, negative and positive rates are undesirable and that data is imbalanced. Adjusted the data.

   ## Best Forest Iteration
   <img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/160342282/82f54208-15d4-4e0a-8a57-a6db36f08629" width="600">

   
   


   



