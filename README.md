# Bellabeat Case Study

## Introduction
Bellabeat is a high-tech manufacturer of health-focused products for women, offering products such as the Bellabeat app, Leaf, Time watch, and Spring. The company is a successful small business with the potential to become a major player in the global smart device market. Analyzing smart device fitness data can help unlock new growth opportunities for Bellabeat.

---

## Business Task
The main objective of this project is to analyze smart device data to gain insights into how consumers are using their devices. Discovering trends in smart device usage can guide Bellabeat’s future marketing strategies and product development.

---

## Key Stakeholders
- Urška Sršen: Co-founder and Chief Creative Officer  
- Sando Mur: Mathematician and Co-founder; key executive team member

---

## Data
The analysis uses the **Fitbit Fitness Tracker dataset** available on [Kaggle](https://www.kaggle.com/arashnic/fitbit).  

Key points:  
- Dataset contains personal fitness tracker data from 30 Fitbit users  
- Includes minute-level output for physical activity, heart rate, and sleep monitoring  
- Covers daily activity, steps, calories, and sleep  
- Collected via Amazon Mechanical Turk between March 12, 2016 and May 12, 2016  
- Public domain license (CC0)  

The dataset contains 18 CSV files. Main files used:  
- `dailyActivity_merged.csv`  
- `dailyCalories_merged.csv`  
- `dailySteps_merged.csv`  
- `sleepDay_merged.csv`  

---

## Data Processing
- Dataset downloaded to **Google BigQuery** for processing due to its size  
- SQL queries used to check data integrity, remove duplicates, and analyze relationships  
- Key checks included:
  - Number of unique IDs per table  
  - Identification of missing values in `sleepDay_merged.csv` (6 missing IDs)  
- Tables with inconsistencies: `dailyActivity_merged.csv`, `dailyCalories_merged.csv`, `dailySteps_merged.csv`, `sleepDay_merged.csv`

---

## Analysis
- Explored relationships between **activity level** and **sleep patterns**  
- Queries joined activity and sleep tables on `Id` and `ActivityDate`  
- Calculated metrics such as active vs. sedentary minutes, distance, and calories burned  

---

## Visualisation
- Data visualised using **R programming**  
- Visualizations include:  
  - Sleep duration and patterns  
  - Activity levels vs. calories burned   

---

## Key Insights
- Average sleep per user: 419.5 minutes (~7 hours)  
- Average time in bed: 458.6 minutes (~7.6 hours), with ~38.6 minutes awake  
- Positive correlation between calories burned and sedentary minutes  

---

## Recommendations
- Add an **alert function** in the Bellabeat app for users with high sedentary minutes  
- Enhance the **sleep tracking feature** to encourage quality sleep  
- Introduce a **reward system** for users meeting daily goals (e.g., 10,000 steps)

---

## Tools Used
- **Google BigQuery / SQL** – Data processing and analysis  
- **R Programming** – Data visualization  


---

## References
- Fitbit dataset: [Kaggle](https://www.kaggle.com/arashnic/fitbit)  
- Data collection via Amazon Mechanical Turk, 2016  
