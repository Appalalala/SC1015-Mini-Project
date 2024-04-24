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
The dataset is from Kaggle, by Sourav Banerjee, titled "Heart Attack Risk Prediction Dataset".
Link : https://www.kaggle.com/datasets/iamsouravbanerjee/heart-attack-prediction-dataset/data

## Context
According to the World Health Organisation, cardiovascular disease is the leading cause of death globally, taking an estimated 17.9 million lives yearly, 32% of global deaths, and 85% were due to heart attacks.
In Singapore, it is reported 11631 heart attack cases per 100k people (7,344 in 2010), averaging 31 a day. Among them, 9.2% died within 30 days.

Up to 80% of premature heart attacks can be prevented with risk management


## Problem Statement
To find out how do the different factors affect the heart attack risk among individuals


## Data
The following is the factors we will be looking at

<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/20bdfa97-275f-4b1a-acae-7ac35b32b274" width="450">

## Data Cleaning
1. Blood pressure data consists of both systolic blood pressure level and diastolic blood pressure level separated by a /.
We initialise 2 new variables Systolic_Blood_Pressure and Diastolic_Blood_Pressure.
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/bf3ea47f-fecd-4fd8-85c7-99fe8cf41bcb" width="450">

2. We drop these 4 factors
   - Patient ID : irrelevant
   - Country & Hemisphere : Are better represented by continent to show distribution of the participations
   - Blood Pressure : Split into Systolic and Diastolic Blood Pressure earlier
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/7f3828d5-a035-4b0b-accd-e2410194147e" width="400">

3. Remove Outliers
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/f20cac37-4677-45fe-8f58-9beaf7397aae" width="400">
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/6da3ae39-608c-4b12-b170-435404959b1d" width="400">

4. Ensure that our data is non-null

## Categorising Variables into 4 Categories 
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/a4c98fac-a3a1-43fd-9498-1084f1ea7ab5" width="400">

## Heat Maps to show Correlation
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/96a7423a-be66-40aa-944d-b3be972c59ff" width="400">
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/0d4ad86f-b1c9-4966-97f4-b9f1cf149420" width="400">

## Variables Chosen from Each Category
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/153801ad-e569-4f31-a208-9fe2ddf0651f" width="400">


### 1. Income Level
People with higher Income Level tend to have a lower Heart Attack Risk
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/542909d0-089d-45aa-971a-2b38ee0facbb" width="400">

### 2. Systolic Blood Pressure
Higher Systolic Blood Pressure points to a higher Heart Attack Risk
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/6fc03755-50ed-4f51-b2a3-80f40db63890" width="400">

### 3. Cholesterol
Higher cholesterol tends to lead to a higher Heart Attack Risk
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/0dfdc227-a1e5-4a8a-bdbb-258310b1ed79" width="400">

### 4. Medication Use
Despite having the highest correlation value under Medical History sub-categorical group, Medication Use does not affect Heart Attack Risk
<img src="https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/0224b965-a5c4-4899-955a-b08e67942957" width="400">


## Our Mission
To accurately classify the Heart Attack Risk (0 or 1) of an individual based on these factors using Machine Learning 
