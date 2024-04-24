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
![Screenshot 2024-04-24 at 5 51 56 PM](https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/20bdfa97-275f-4b1a-acae-7ac35b32b274)

## Data Cleaning
1. Blood pressure data consists of both systolic blood pressure level and diastolic blood pressure level separated by a /.
We initialise 2 new variables Systolic_Blood_Pressure and Diastolic_Blood_Pressure.
![Screenshot 2024-04-24 at 5 56 29 PM](https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/bf3ea47f-fecd-4fd8-85c7-99fe8cf41bcb)


2. We drop these 4 factors
   - Patient ID : irrelevant
   - Country & Hemisphere : Are better represented by continent to show distribution of the participations
   - Blood Pressure : Split into Systolic and Diastolic Blood Pressure earlier
![Screenshot 2024-04-24 at 5 56 59 PM](https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/7f3828d5-a035-4b0b-accd-e2410194147e)


3. Remove Outliers
![Screenshot 2024-04-24 at 5 56 45 PM](https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/f20cac37-4677-45fe-8f58-9beaf7397aae)
![Screenshot 2024-04-24 at 3 33 00 PM](https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/6da3ae39-608c-4b12-b170-435404959b1d)

4. Ensure that our data is non-null
![Screenshot 2024-04-24 at 5 57 14 PM](https://github.com/harikrishnan-vinod/SC1015-Mini-Project/assets/161003075/a9ec8b2b-05ef-4697-befb-86c1c03e5e64)
