# Healthcare Analytics: Financial, Operational & Clinical Performance Dashboard

## Introduction

This project presents an end-to-end Healthcare Analytics Dashboard designed to evaluate operational performance, clinical quality, financial viability, 
and patient risk profiles across hospital networks. By consolidating complex hospital admission, billing, and clinical outcome metrics into interactive visual modules,
this project enables healthcare administrators, clinical directors, and financial managers to make data-driven decisions.

The analysis spans three primary dimensions:
1. Financial and Revenue Performance: Tracking overall revenue generation, billing distribution per condition, and insurance provider contributions.
2. Operational and Facility Efficiency: Evaluating bed utilization, length of stay (LOS), admission trends, and age-group demographics.
3. Clinical Quality & Patient Risk Evaluation: Monitoring abnormal test rates, high-risk patient cohorts, and medication-specific risk patterns.
   
## Business & Operational Questions
### Financial Metrics:
  <img width="1920" height="1080" alt="Screenshot 2026-10-06 161223" src="https://github.com/user-attachments/assets/f7eb663a-a6aa-4e70-a5a3-9282f7f2f54c" />

 1. What is the total revenue generated, and what is the average billing per patient admission?
 2. Which medical conditions incur the highest average billing per case?
 3. How balanced is the revenue distribution across major insurance providers?
 4. Which hospital entities lead in average billing per case?
## Operational Efficiency:
<img width="1920" height="1080" alt="Screenshot 2026-10-08 090013" src="https://github.com/user-attachments/assets/6bbf0ff6-c3c4-4dd6-bab9-4fb1c5e847bd" />

1. What is the average length of stay (LOS) across various medical conditions?
2. How are hospital admissions distributed across age groups (Pediatric, Adult, Senior, Elderly)?
3. What are the seasonal or monthly admission trends throughout the year?
## Clinical & Risk Evaluation:
<img width="1920" height="1080" alt="Screenshot 2026-10-06 161241" src="https://github.com/user-attachments/assets/7e79642f-79ae-4770-8071-5687342798da" />

1. What proportion of patient admissions belong to the high-risk cohort, and what is the abnormal test result rate?
2. Which age groups represent the highest proportion of high-risk cases?
3. Which medical conditions and medications account for the largest volume of abnormal test outcomes?
4. Which hospital networks exhibit the highest percentage of high-risk patients?

## Data Preprocessing
Extensive data cleaning and validation were performed using SQL queries and data modeling techniques to ensure analytical rigor:
1. Null & Duplicate Handling: Identified and removed duplicate records across patient registries, admission logs, and billing files.
2. Data Type Conversion: Standardized date formats (Admission Date, Discharge Date) and converted monetary values (Billing Amount) into standard numeric datatypes.
3. Demographic Grouping: Categorized patient ages into explicit demographic cohorts: Pediatric (<18), Adult (18-50), Senior (51-70), and Elderly (70+).
4. Calculated DAX & SQL Measures: Created calculated columns and DAX measures for Length of Stay (Discharge Date - Admission Date),
   High-Risk Cohort Flags, Abnormal Test Outcome Rates, and Revenue Percentages.

## Methodology
1. Database Querying & Extraction: Extracted raw healthcare datasets using SQL to perform aggregations, window functions, and multi-table joins.
2. Data Modeling: Established a star schema relational model linking Patient Demographics, Admission Records, Facility Profiles, and Billing Data.
3. Interactive Visualizations: Built three integrated dashboard pages in Power BI featuring slicers for year-over-year dynamic filtering, medical condition selectors, and facility drill-downs

## Key Metrics & Integrated Dashboard Insights
Dashboard View 1: Financial & Revenue Performance
1. Total Revenue: $1.42 Billion across 56,000 Total Admissions.
2. Average Billing Per Case: $25.54K.
3. Condition-Level Billing: Remarkably consistent across conditions: Obesity ($25.81K), Asthma ($25.64K), Diabetes ($25.64K), Arthritis ($25.50K), Hypertension ($25.50K), and Cancer ($25.16K).
4. Admission Type Breakdown: Revenue is evenly distributed between Elective ($477.61M), Urgent ($474.01M), and Emergency ($465.81M) care.
5. Insurance Market Share: Balanced contribution across top providers—Cigna (20.26%), Medicare (20.16%), Blue Cross (19.98%), UnitedHealthcare (19.93%), and Aetna (19.67%).
6. Facility Billing Leaders: Inc Brown recorded the highest average billing per case at $32K, followed by Smith PLC ($29K) and Johnson PLC ($29K).
## Dashboard View 2: Operational & Facility Efficiency
1. Average Length of Stay (LOS):
  16 Days on average, Asthma and Arthritis patients average 16 days, while Cancer, Obesity, Hypertension, and Diabetes average 15 days
2. Demographic Volume Split:
  Adults (18–50): 20,327 admissions (36.3%).
  Elderly (70+): 17,424 admissions (31.1%).
  Seniors (51–70): 17,251 admissions (30.8%).
  Pediatrics (<18): 498 admissions (0.9%)
4. Monthly Admission Patterns: Peak admission volume occurred in July (4,793) and August (4,765), with lower volume observed in February (4,319) and November (4,523).
5. Top Hospital Admissions: LLC Smith led facility throughput with 44 admissions, followed by Ltd Smith (39) and Johnson PLC (38).
## Dashboard View 3: Clinical Quality & Patient Risk Evaluation
1. High-Risk Cohort: 12,000 High-Risk Patients representing 29.56% of total admissions.
2. Abnormal Test Rate: 33.56% overall abnormal result rate (19,000 Abnormal Test Count).
3. High Risk by Age Cohort: Adults (18–50) represent the highest volume of high-risk cases (4,570), followed by Seniors (3,758) and Elderly (3,440).
4. Abnormal Test Drivers: Arthritis (3,188 tests) and Diabetes (3,168 tests) logged the highest count of abnormal outcomes.
5. Hospital Risk Ratios: Ltd Smith recorded the highest concentration of high-risk patients at 40.00%, followed by Smith Group (37.50%) and LLC Smith (32.50%).

## Recommendations
1. Optimize Discharge Management: Develop clinical care pathways to shorten length of stay (LOS) for chronic conditions like Asthma and Arthritis to increase overall bed availability.
2. Targeted High-Risk Interventions: Implement specialized disease management and preventive protocols for the Adult (18–50) and Senior demographics, who account for the largest volume of high-risk patients.
3. Clinical Quality Audits: Conduct targeted quality reviews at outlier facilities (e.g., Ltd Smith with a 40.00% high-risk cohort) to ensure standard care protocols and diagnostic accuracy
4. Payer & Revenue Strategy: Maintain balanced payer networks while standardizing billing structures across lower-performing hospital facilities.

## Conclusion
This unified Healthcare Analytics project transforms complex operational, clinical, and billing data into direct strategic intelligence.
By connecting financial performance metrics with length-of-stay drivers and patient risk profiles, hospital leaders can improve clinical care delivery, 
optimize facility efficiency, and maintain strong financial sustainability. 

Author: Michael Daniel Odoh 
