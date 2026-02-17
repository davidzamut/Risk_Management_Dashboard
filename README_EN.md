# 🏦 Credit Risk Analytics Dashboard

![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Tool](https://img.shields.io/badge/Tool-Power%20BI-F2C811?logo=powerbi&logoColor=black)
![Data Processing](https://img.shields.io/badge/Data-Power%20Query%20%7C%20DAX-blue)

## Executive Summary
This project delivers an interactive Power BI dashboard designed to analyze and monitor credit risk across the bank's client portfolio. 

Instead of a black-box predictive model, this tool empowers decision-makers to visually identify high-risk segments, monitor key financial ratios (like Debt-to-Income), and understand the profile of clients who default, ultimately aiming to minimize financial losses and optimize the loan approval strategy.

---

## 1. Business Understanding

### The Problem
Financial institutions lose millions annually due to "Bad Debt" (non-performing loans). Without clear, real-time visibility into the characteristics of defaulting clients, risk managers cannot adjust their credit policies effectively.

### Objectives
1.  **Identify Risk Drivers:** Uncover demographic and financial patterns associated with loan defaults (`TARGET = 1`).
2.  **Portfolio Monitoring:** Provide a high-level view of total credit exposure and current default rates.

### Success Metrics (KPIs)
* **Total Exposure ($):** Total amount of credit at risk.
* **Default Rate (%):** Percentage of loans that have defaulted.
* **Average Credit-to-Income Ratio:** Monitoring client leverage.
* **Years to Pay Debt:** Monitoring risk factors associated with loan duration. 

---

## 2. Data Overview
**Source:** [Kaggle: Application Data](https://www.kaggle.com/datasets/dssouvikganguly/application-datacsv)  
**Dimensions:** 455k+ rows, 122 columns.

### Key Variables:
* `TARGET`: 1 = Customer whose loan was approved, 0 = Denied loan.
* `AMT_INCOME_TOTAL`: Client's total income.
* `AMT_CREDIT`: Credit amount of the loan.
* `NAME_EDUCATION_TYPE`: Client's highest level of education achieved.

---

## 3. Methodology & Data Modeling
This project follows a standard Business Intelligence workflow:

1.  **Data Ingestion & Transformation (via CSV):** * Cleaned missing values and standardized text fields.
    * Created conditional columns for age groups and income brackets.
2.  **Data Modeling:** * Due to the dataset's structure, a complex data modeling phase was not required, as all features corresponded to a single customer flat table.
3.  **DAX Measures:** * Developed custom DAX measures for dynamic KPIs (e.g., Year-to-Date defaults, moving averages, dynamic segmentation).
4.  **Dashboard Design:** * Built an intuitive UI focusing on user experience (UX), utilizing cross-filtering, tooltips, and drill-through features for deep-dive analysis.

---

## 4. Key Insights

* *There are a total of 63 high-risk approved loans that sum up to $68.27 million in possible losses.*
* *There are around 3,789 unapproved, low-risk, high-value loans that represent $860.4 million in missed possible earnings.*
* *No significant demographic distinctions or correlations were found in this analysis.*

---

## 5. How to Interact with this Project

### Viewing the Dashboard
* **Local Option:** 1. Clone this repository.
  2. Ensure you have [Power BI Desktop](https://powerbi.microsoft.com/desktop/) installed.
  3. Open the `Credit_Risk_Dashboard.pbix` file located in the `dashboards/` folder.

### Repository Structure
