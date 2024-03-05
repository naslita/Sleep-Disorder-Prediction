
# **🌟 Sleep Disorder Prediction - Final Project Dibimbing 🌟**

<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/main/Sleep Disorder Bg.png">


## **⛳ Introduction⛳**

In our busy working lives, we often underestimate the significance of prioritizing a healthy lifestyle. Yet, sleep is undeniably vital for our overall health and wellness. Incorporating elements like a balanced diet, consistent exercise, and stress management can profoundly improve the quality of our sleep, thereby safeguarding our heart health.


## **📍 Table of Content 📍**
<!--ts-->
* **Business Understanding**
    * [Problem Statement](#-business-understanding-)
    * [Goals](#-goals)
    * [Objectives](#-objectives)
* **Data Understanding**
    * [Data Description](#-data-understanding-)
    * [Metadata](#-metadata)
* **Data Preparation**
    * [Data Cleansing](#-data-preparation-)
    * [Encoding](#-data-preparation-)
    * [Imbalance & Standardization](#-data-preparation-)
    * [Correlation Analysis](#-data-preparation-)
* **Exploratory Data Analysis**
    * [Relate By Gender](#-exploratory-data-anaylsis)
    * [Relate By Occupation](#-occupation)
    * [Relate By Physical Activity Level](#-physical-activity-level)
    * [Relate By Quality of Sleep](#-quality-of-sleep)
    * [Relate By Sleep Duration](#-sleep-duration)
    * [Relate By Stress Level](#-stress-level)
    * [Relate by Heart Rate](#-heart-rate)
    * [Relate by Daily Steps](#-daily-steps)
    * [Relate By BMI Category](#-bmi-category)
    * [Relate by Age](#-age)
    * [Relate by Blood Pressure](#-blood-pressure)
* **Preprocessing**
    * [Preprocessing](#-preprocessing)
    * [Heatmap Correlation](#-heatmap-correlation)
* **[Modelling](#-modelling)**
* **[Evaluation](#-evaluation)**
* **[Insight & Recommendation](#-insight-&-recommendation)**

<!--te-->


## **💻 Script 💻**

**Open in Colab**

- [Sleep-Disorder-Prediction.ipynb](Finpro_Anastasia_Talia_Dwimantari.ipynb)

**Libraries**

[Requirements Text](Library)

**Dataset**

[Sleep Health and Lifestyle Dataset](https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset/data)



## **⚙ Work Environment ⚙**

- **Tools**

[![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)](https://jupyter.org/try)

[![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](Finpro_Anastasia_Talia_Dwimantari.ipynb)

- **Programming Language**

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)

[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)


## **⛳ Business Understanding ⛳**

### **📌 Problem Statement**

**Sleep Disorder** encompass conditions stemming from unhealthy sleep habits and lifestyles. Neglecting proper sleep can pose significant risks to our health and well-being, as sleep plays a pivotal role in maintaining overall health. Research from the National Heart, Lung, and Blood Institute of the National Institutes of Health indicates that between 50 to 70 million American adults grapple with irregular sleep patterns or suffer from disorders like insomnia and sleep apnea, underscoring a prevalent issue in our society.

Drawing from the aforementioned facts, **adhering to a balanced diet**, **maintaining regular exercise**, and **effectively managing stress levels emerge** as pivotal strategies for preventing sleep disorders.

### **📌 Goals**

- Discover factors impacting sleep health and lifestyle for detecting signs of sleep disorders.
- Predict the likelihood of individuals experiencing sleep disorders using their sleep health and lifestyle data.
- Identify and address sleep-related issues, especially in healthcare.
- Obtain the optimal model for predicting sleep disorders. 


### **📌 Objectives**

Develop a classification model to **anticipate the primary factors contributing to sleep disorders**, **facilitating the prompt detection and prevention of such disorders**.

**📝 References :**

1. Understanding Blood Pressure Readings: [https://www.heart.org/en/health-topics/high-blood-pressure/understanding-blood-pressure-readings](https://www.heart.org/en/health-topics/high-blood-pressure/understanding-blood-pressure-readings)

2. Sleep Apnea Statistics: [https://www.ncoa.org/adviser/sleep/sleep-apnea-statistics/](https://www.ncoa.org/adviser/sleep/sleep-apnea-statistics/)

3. Physical Activity Basics for Adults: [https://www.cdc.gov/physicalactivity/basics/adults/index.htm](https://www.cdc.gov/physicalactivity/basics/adults/index.htm)

4. The Basics of Decision Trees: [https://medium.datadriveninvestor.com/the-basics-of-decision-trees-e5837cc2aba7](https://medium.datadriveninvestor.com/the-basics-of-decision-trees-e5837cc2aba7)

5. Classification in Decision Trees - A Step-by-Step CART (Classification and Regression Tree): [https://medium.com/analytics-vidhya/classification-in-decision-tree-a-step-by-step-cart-classification-and-regression-tree-8e5f5228b11e](https://medium.com/analytics-vidhya/classification-in-decision-tree-a-step-by-step-cart-classification-and-regression-tree-8e5f5228b11e)

6. Heart Rate FAQ: [https://www.mayoclinic.org/healthy-lifestyle/fitness/expert-answers/heart-rate/faq-20057979#:~:text=A%20normal%20resting%20heart%20rate%20for%20adults%20ranges%20from%2060,to%2040%20beats%20per%20minute.](https://www.mayoclinic.org/healthy-lifestyle/fitness/expert-answers/heart-rate/faq-20057979#:~:text=A%20normal%20resting%20heart%20rate%20for%20adults%20ranges%20from%2060,to%2040%20beats%20per%20minute.)

## **🕹 Data Understanding 🕹**

**Sleep Disorder ([link datasets](https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset/data))**


**Dataset Description:**

- The dataset contains `374 samples` and `13 features`, with `1 target` feature `"Sleep Disorder"`
- The dataset consists of 3 types of data types: `int64`, `object`, and `float64`.

**Metadata**

- `Personal ID` - An identifier for each individual
- `Gender` - The gender of the person (Male/Female)
- `Age` - The age of the person in years
- `Occupation` - The occupation or profession of the person
- `Sleep Duration (hours)` - The number of hours the person sleeps per day.
- `Quality of Sleep (scale: 1-10)` - A subjective rating of the quality of sleep, ranging from 1 to 10
- `Physical Activity Level (minutes/day)` - The number of minutes the person engages in physical activity daily
- `Stress Level (scale: 1-10)` - A subjective rating of the stress level experienced by the person, ranging from 1 to 10
- `BMI Category` - The BMI category of the person (e.g., Underweight, Normal, Overweight)
- `Blood Pressure (systolic/diastolic)` - The blood pressure measurement of the person, indicated as systolic pressure over diastolic pressure
- `Heart Rate (bpm)` - he resting heart rate of the person in beats per minute.
- `Daily Steps` - The number of steps the person takes per day.
- `Sleep Disorder` - The presence or absence of a sleep disorder in the person (None, Insomnia, Sleep Apnea)

## **💡 Data Preparation 💡**

### **Data Cleansing**

<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/main/Missing Value.png">

#### **Checking Missing Values**

- No Missing Values

#### **Checking Duplicate Rows**

- No Duplicate

#### **[Checking Data types](#-data-understanding-)**

<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/main/Statistical Summary Num.png">

<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/main/Statistical Summary Cat.png">

#### **Statistical Summary**
*Considering the distribution of all numerical variables, they exhibit a positive skew toward the right*

Observation Summary Numerical:
* Overall, the minimum and maximum values make sense for each column
*`Age`, `Sleep Duration`, `Quality of Sleep`, `Physical Activity Level`,`Stress Level`,`Heart Rate` and `Daily Steps` are discrete values with any unique values, need to conclude its simmetricity either.
* Mean != 50% (Median) in `Sleep Duration`, `Quality of Sleep`, `Physical Activity Level`,`Stress Level`,`Heart Rate` and `Daily Steps`column, shows a positive direction distribution

Observation Summary Categorical:
* `Gender` has 2 unique values: 'Male' and 'Female'.
* `Job` has 11 unique values: 'Nurse', 'Doctor', 'Engineer', 'Lawyer', 'Teacher', 'Accountant', 'Salesperson', 'Software Engineer', 'Scientist', 'Sales Representative', and 'Manager'.
* `BMI Category` has 3 unique values: 'Normal', 'Overweight', and 'Obesity'.
* `Blood Pressure` has 25 unique values and the most is 130/85.
* `Sleep Disorders` has 3 unique values: 'None', 'Sleep Apnea', and 'Insomnia'.
* From the categorical data, the following can be observed:
1. While there are more male individuals, the difference compared to females is not very significant, with only a discrepancy of 4 individuals.
2. There are more individuals in nursing jobs, but the difference is not significantly greater than other professions.
3. More individuals fall into the BMI category 'Normal', but the difference is not significantly greater than other BMI categories.
4. More individuals do not have sleep disorders, but the difference is not significantly greater than those who do have sleep disorders.
* In terms of the target variable, `Sleep Disorder = None` (any specific sleep disorder) is more frequent in the dataset. But, the imbalance condition is NOT severe (still OK)

#### **Change Normal Weight to be Normal**

#### **Univariate and Bivariate Analysis**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/KDE Plot.png">

#### **Handling Outlier**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/Univariate.png">

### **[Encoding](#-preprocessing)**

### **Imbalance & Standardization**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/Oversampling.png">

### **[Correlation Analysis](#-Heatmap)**

## **📌 Exploratory Data Analysis (EDA)**

### **Gender**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/EDA Gender.png">

### **Occupation**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/EDA Occupation.png">

### **Physical Activity Level**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/EDA PAL.png">

### **Quality of Sleep**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/EDA QOS.png">

### **Sleep Duration**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/EDA SD.png">

### **Stress Level**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/EDA SL.png">

### **Heart Rate**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/EDA HR.png">

### **Daily Steps**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/EDA DS.png">

### **BMI Category**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/EDA BMI.png">

### **Age**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/EDA Age.png">

### **Blood Pressure**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/EDA BP.png">

## **💡Preprocessing💡**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/Prepocessing.png">

### **Heatmap Correlation**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/Headmap 1.png">
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/Headmap 2.png">

## **💡Modelling💡**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/Hypertuning DTC.png">

## **💡Evaluation💡**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/train test dtc.png">
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/Confusion Matrix.png">
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/ROC Curve dtc.png">
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/Learning Curve.png">

### **Feature Importance**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/Feature Importance.png">
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/Shap Method.png">

## **💡Insight & Recommendation💡**
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/Recommendation 1.png">
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/Recommendation 2.png">
<img src="https://raw.github.com/naslita/Sleep-Disorder-Prediction/Master/Recomendation 3.png">
