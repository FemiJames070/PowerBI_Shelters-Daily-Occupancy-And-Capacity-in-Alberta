# 📊 Alberta Emergency Shelters: Capacity & Occupancy Predictive Analysis

[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Data_Analysis_Expressions-blue?style=flat)](#)
[![Data Analytics](https://img.shields.io/badge/Data_Analytics-Business_Intelligence-00599C?style=flat)](#)

## 📖 Project Overview
This Business Intelligence project analyzes historical shelter usage patterns across Alberta, Canada, from 2013 to 2024. As the demand for emergency shelter services fluctuates, this analysis transitions from descriptive reporting to diagnostic and predictive modeling using Power BI and DAX. The goal is to uncover utilization trends, forecast future operational demands for 2025–2026, and identify specific cities and organizations at risk of critical overcapacity.

**Data Source:** [Funded Emergency Shelters Daily Occupancy (Open Alberta)](https://open.alberta.ca/opendata/funded-emergency-shelters-daily-occupancy-ab/resource/b7080b66-25ea-4c30-ac47-02b64353637f)

## 🎯 Business Understanding & Core Questions
Beyond simply mapping historical data, this project was engineered to provide strategic foresight for resource allocation and emergency planning by answering two critical questions:
1. **Capacity Forecasting:** Will a projected 20% yearly increase in occupancy through 2026 exceed available structural capacity?
2. **Risk Identification:** Which cities and specific organizations face the highest (and lowest) risk of critical shelter overcapacity during peak demand periods?

## ⚙️ Methodology & Diagnostic Insights
The dataset encompasses total approved beds, SCSS-funded beds, winter emergency response beds, and daily occupancy. 

### Trend Analysis (2013–2024)
* **The Widening Gap:** While shelter capacity steadily increased from 1.14M (2013) to a peak of 1.50M (2022), overnight occupancy gradually declined after 2014, stabilizing around 1.16M in 2024. In aggregate, capacity (17M) significantly outpaces historical overnight occupancy (13M), representing an overall 43% utilization rate.
* **Geographic & Organizational Concentration:** Calgary dominates both infrastructure (6M capacity) and demand (4M occupancy). The Calgary Drop-In Centre holds the highest capacity (2.52M), while organizations like Hope Mission and Mustard Seed Calgary operate with very tight capacity-to-occupancy margins.

### Diagnostic Statistical Modeling
To validate the data for future forecasting, a regression analysis was performed on the relationship between Capacity and Occupancy:
* **High Correlation:** An R-squared value of **0.9331** confirms a very strong, predictable relationship between shelter capacity and occupancy. 
* **Scaling Metric:** A slope of **0.7353** indicates that for every 1-unit increase in Capacity, the expected Overnight Occupancy increases by ~0.74 units, confirming that while occupancy scales with capacity, available space is generally underutilized in aggregate.

## 📈 Predictive Findings (Answering the Business Questions)

Advanced DAX measures were engineered to forecast 2025/2026 scenarios and calculate localized risk factors.

### 1. 2026 Overcapacity Forecast
*Scenario: A 20% year-over-year increase in occupancy.*
**Conclusion: YES.** While aggregate provincial capacity may hold, specific organizations will critically exceed their limits by 2026:
* **Homelessness Society of the Bow Valley (Bow Valley):** Projected 117.21% Capacity Utilization
* **Mustard Seed (Calgary):** Projected 115.20% Capacity Utilization
* **Niginan Housing Ventures (Edmonton):** Projected 100.75% Capacity Utilization

### 2. Peak Demand Risk Factor Analysis
By leveraging DAX to calculate a custom `Risk Factor (%)` based on maximum historical peak occupancies, extreme vulnerabilities were isolated:
* **Highest Risk (Critical Overcapacity Danger):**
  * Elizabeth House (Edmonton): **754.17% Risk Factor**
  * Elders Caring Centre (Grande Prairie): **319.44% Risk Factor**
  * Mustard Seed (Edmonton) & The Alex (Calgary): Also flagged over the 100% risk threshold.
* **Lowest Risk (Stable during Peaks):**
  * Wapiti Community Support Association (Grande Prairie): 0.01% Risk Factor
  * Operation Friendship (Edmonton): 0.02% Risk Factor

## 🚀 Strategic Recommendations
Based on the predictive DAX models, the following actions are recommended for stakeholders:
1. **Targeted Resource Allocation:** Immediately prioritize funding, expansion, and winter-response support for the severely high-risk shelters identified in Edmonton, Grande Prairie, and Calgary.
2. **Early Warning Systems:** Utilize this predictive modeling framework to monitor quarterly occupancy velocities, automatically flagging organizations approaching the 100% Risk Factor threshold before winter peak seasons.
3. **Policy Review:** Investigate the massive capacity-to-occupancy gap at the aggregate level. Redirect resources from consistently underutilized networks to the localized organizations identified as operating beyond safe capacities.

## 📂 Repository Contents
To ensure full accessibility for both technical and non-technical stakeholders, the reporting files are provided in multiple formats:
* `Emergency_Shelters_Analysis.pbix`: The complete, interactive Power BI Desktop file containing all data models, DAX measures, and interactive visualizations.
* `Emergency_Shelters_Report.pdf`: A static, accessible export of the final dashboard for quick executive review.

**✍️ Author**
Femi James
Data & Business Analyst | Integrated AI Specialist
