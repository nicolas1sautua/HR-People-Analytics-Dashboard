# Executive People Analytics: Employee Attrition & Retention Suite

## Project Overview
This project builds a complete end-to-end Business Intelligence and People Analytics solution designed to identify the root causes of voluntary employee turnover. By pairing data engineering in Python with interactive visual storytelling in Tableau, this suite transforms raw operational workforce logs into data-driven strategies for corporate leadership.

**📊 Live Interactive Dashboard:** https://public.tableau.com/app/profile/nicolas.sautua6141/viz/HRPeopleAnalytics-EmployeeAttritionDashboard/HRPeopleAnalytics-EmployeeAttritionDashboard 

## Technical Architecture & Workflow
1. **Data Sanitization & Engineering (Python):** * Ingested and audited workforce profiles via `Pandas`.
   * Checked for structural anomalies, confirmed zero missing values, and dropped redundant operational variables to optimize dashboard query performance.
   * Mapped numerical attributes to descriptive categorical strings (`JobSatisfaction_Label`, `WorkLifeBalance_Label`) to improve end-user visual comprehension.
  
2. **Metric Formulations (Excel/Tableau Calculated Fields):**
   * Engineered the primary corporate North Star KPI utilizing a calculated aggregation:
     $$\text{Attrition Rate} = \frac{\text{COUNT}(\text{IF Attrition} = \text{'Yes' THEN } 1\text{ END})}{\text{COUNT}(\text{Attrition})}$$
     
3. **Interactive BI Visualizations (Tableau):**
   * Designed a unified, automatic-scaling executive dashboard layout.
   * Implemented discrete color alerting frameworks to highlight extreme behavioral disparities.
   * Embedded interactive cross-filtering, allowing stakeholders to dynamically slice the organizational data by operational variables.

## Executive Interactive Dashboard
![Executive HR Dashboard](HR%20People%20Analytics%20-%20Employee%20Attrition%20Dashboard.png)

## Repository Contents
* `employee_attrition.csv`: Raw, baseline corporate dataset.
* `HR_Cleaned_Data_For_Tableau.csv`: The finalized dataset generated via feature engineering.
* `HR_Attrition_Analysis.ipynb`: The documented Google Colab Python notebook containing the EDA script.
