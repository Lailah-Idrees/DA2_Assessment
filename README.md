# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

## Stroke Predicitions Data Analysis 

Stroke Predictions Data Analysis is a comprehensive data analysis tool designed to streamline data exploration, analysis, visualisation and machine learning. The tool supports multiple data formats and provides an intuitive interface for both novice and expert data scientists.



## Dataset Content

This dataset contains stroke predictors for individuals, along with key demographic and lifestyle attributes such as age, BMI, sex, children, age and smoking status. The original dataset consists of 5,110 rows and 12 columns and was sourced from Kaggle link [here](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset).

During the ETL phase of the data analysis process, additional features were created and added to the dataset. As a result, the final dataset includes the following columns:

* Age
* Hypertension
* Heart Disease
* Avergae Glucose Level
* BMI
* Weight Category
* Ever Married
* Ever Married Yes
* Work Type
* Work Type Encoded
* Residence Type
* Residence Type Urban
* Smoking Status

## Aim of Analysis
The aim of this project is to investigate how demographic, lifestyle, and health‑related variables influence stroke outcomes, and to develop a machine‑learning model capable of predicting whether an individual is likely to experience a stroke.

## PowerBI Dashboard 
The link to the Stroke Predictions Dashboard can be found [here](https://app.powerbi.com/groups/me/reports/9b285b2a-8ee0-4029-a00a-9fe32e0bc3e2/c1541ac4e3238de7c32e?experience=power-bi)

## Hypothesis
**H1: Age and Health Conditions**

There will be a positive correlation between age and the likelihood of experiencing stroke, heart disease, or hypertension.
Older individuals are generally more susceptible to severe health conditions due to physiological decline.

* This hypothesis was supported by the exploratory analysis: scatterplots and stripplots showed that stroke, heart disease, and hypertension cases were concentrated in older age groups, and the correlation heatmap confirmed moderately positive correlations between age and stroke (0.25), age and heart disease (0.26), and age and hypertension (0.28).


**H2: Age and BMI**

There will be a weak negative correlation between age and BMI.
As people age, metabolic rate tends to slow and appetite may decrease, which can lead to slightly lower BMI values in older adults.

* This hypothesis was based on the assumption that metabolic rate slows with age and appetite may decrease, potentially leading to slightly lower BMI values in older adults. However, the data did not support this expectation. Instead, the analysis revealed a weak positive correlation between age and BMI.

**H3: Cardiovascular Conditions and Stroke**

Individuals with heart disease or hypertension will be more likely to have experienced a stroke.
Both conditions are caused by similar cardiovascular risk factors, and elevated blood pressure or impaired heart function can increase the likelihood of stroke.
* The data did not support this expectation. Instead, the analysis revealed a weak positive correlation between age and BMI. Scatterplots and stripplots showed that BMI tends to increase slightly with age, and the correlation heatmap confirmed this with a small positive correlation coefficient (approximately 0.35).

**H4: BMI and Stroke**

There will be a positive relationship between BMI and stroke incidence.
Higher BMI is associated with increased cardiovascular strain and metabolic risk, which may contribute to a greater likelihood of experiencing a stroke.
* Across every stage of your analysis, BMI showed little to no meaningful relationship with stroke.



## Challenges
**Visualising categorical relationships with a large dataset**

Initial scatterplots were ineffective because the dataset contained thousands of points, causing severe overplotting.

With guidance, striplots were used instead, allowing the categorical relationships to be visualised clearly without losing interpretability.

**Severe class imbalance in the stroke variable**

The dataset contained 4861 non‑stroke cases vs only 249 stroke cases, creating a highly imbalanced target.

This imbalance caused the logistic regression model to favour the majority class, resulting in very low precision and recall for stroke predictions.

The model struggled to correctly identify stroke cases, even when accuracy appeared high.

**Loss of the ‘smoking_status’ variable during data cleaning**

During preprocessing, the smoking_status column was unintentionally removed from the dataset.

Although this did not affect the core analysis, it meant that one potentially important health‑related feature was not included in the modelling stage.

## Future Work
**Address the severe class imbalance in the stroke variable**

collect more data on stroke individuals this will add more data to the dataset and make predicitions more precise.

**Explore more advanced machine‑learning models**

Test algorithms such as Random Forest and Decision trees

Compare model performance using cross‑validated results to ensure reliability.

**Reintroduce and analyse the missing ‘smoking_status’ variable**

Restore or reconstruct the smoking_status feature, as smoking is a known cardiovascular risk factor.

Investigate its relationship with stroke, heart disease, and hypertension to determine whether it improves model performance or interpretability.

**Add More Functions**
A lot of similar plots were constructed using custom fucntions can reduce the amount of code visible on the screen making it feel less cluttered. I would therefor incorperate more function in my future work
