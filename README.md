# HR Attrition Analytics Dashboard

## ↪️Project background:
This dataset is one of the most widely used HR analytics datasets.  
I wanted to put **my own spin** on it by creating a **clean, clutter-free dashboard** that delivers **maximum insight with minimum noise**.  

I also implemented a modern ETL approach using **Dataflow Gen2**, which acts as the data preparation pipeline before the model loads into Power BI.  
(Scroll down to learn more.)

Thanks for stopping by — hope you enjoy the project!
## 📚Table of Contents:

|**No.**  |**Section**|
|:-: | :------------ | 
|1.   |  [Project Objective and What It Solves](#project-objective-and-what-it-solves)                              |
|2.   |  [Dataset Overview](#dataset-overview)                              |
|3.   |  [Data Pipeline (Dataflow Gen2)](#data-pipeline-(dataflow-gen2))                              |
|4.   |  [Dashboard Highlights](#dashboard-highlights)                              |
|5.   |  [Insights](#insights)                              |
|6.   |  [Recommendations](#recommendations)                              |
## 🎯Project Objective and What It Solves
This project focuses on understanding **why employees leave** and identifying **which segments are most at risk** using a clean, high-information HR Attrition dashboard.

The analysis helps HR answer:
- What is the overall attrition rate?
- Which departments, job roles, or age groups face the highest turnover?
- How do salary, tenure, overtime, and satisfaction influence attrition?
- Which employee segments should HR prioritize for retention efforts?

The goal is simple:  
Deliver **maximum insight with minimal clutter**, using field parameters and a Dataflow Gen2 ETL pipeline.

[(Back to top)](#table-of-contents)

## 🗂Dataset Overview  
A HR dataset containing demographic, job, compensation, and satisfaction variables.  
Key fields include:  
- Age, Gender, Education  
- Department, Job Role, Job Level  
- Monthly Income, Stock Option Level  
- Years at Company, Years in Current Role  
- Job Satisfaction, Work–Life Balance  
- **Attrition (Yes/No)**

The dataset is fully anonymized and safe for public analytics use.

[(Back to top)](#table-of-contents)

## 📊Data Pipeline (Dataflow Gen2)  
I used Microsoft Fabric Dataflow Gen2 as the ETL layer for this project. Its purpose was to create a governed, enterprise-style data pipeline that feeds clean data into Power BI. Key responsibilities included:

- Ingesting raw HR data into Fabric
- Performing data cleaning, transformations, and type conversions
- Creating derived analytical groups such as Age Band, Income Band, and "Distance to work" groups.
- Publishing standardized tables ready for Power BI modeling
- Supporting easy refresh, governance, and reusability across the analytics workflow

To make this pipeline fully functional, I had to learn and configure the **On-Premises Data Gateway**.
Without the gateway, Fabric Dataflows cannot refresh or connect to local/on-premise data sources, so setting it up was essential for automated, reliable data ingestion.

This approach mirrors how *real enterprise* teams build governed pipelines where analysts work from trusted, reusable datasets rather than raw files.

<img src="https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Dataflow%20Gen2%20Lineage.png" height="1000">

#### Demo:
<img src="https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Dataflow%20Gen2.gif" height="1000">

[(Back to top)](#table-of-contents)

## 🖥Dashboard Highlights  
The report is designed with clarity, readability, and high information density at its core.

Key features include:

- **One-page** layout with zero visual clutter
- Smart grouping of demographics, compensation, and job-related insights
- Interactive **field parameters** to switch between views seamlessly
- Clean, modern visuals with a light color palette and minimal text
- Dynamic segmentation to quickly identify high-risk employee groups
- Optimized for **recruiters and HR leaders**, focusing on efficiency and decision-ready insights

The dashboard is published to the *Power BI Service* in a dedicated workspace for easy access, sharing, and collaboration.

![Dashboard](https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Dashboard%20Overview.gif)

[(Back to top)](#table-of-contents)

## 💡Insights

### Education Level

Employees with No Formal Education show the highest attrition, indicating lower retention stability in this group.
This aligns with industry patterns, where employees with fewer formal qualifications often transition more frequently due to limited growth opportunities or early-career mobility.

<img src="https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Attrition%20%25%20by%20Education.png" height="400">

### Age Groups

The 26–35 age group records the highest attrition, reflecting the stage where professionals are most likely to switch roles for career growth, salary progression, or better job alignment.
This age band naturally experiences:

- Increased career mobility
- Exposure to competitive job markets
- Higher expectations for growth and recognition
- Dissatisfaction when career progression stagnates

As a result, employees in this group commonly exhibit the highest turnover.

<img src="https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Attrition%20%25%20by%20Age%20Group.png" height="400">

### Distance to Work

Employees living 0–10 km from the workplace show the highest attrition across distance bands.
Within this group, 32.79% also report working overtime, suggesting a potential connection between workload intensity and turnover.

However, commute distance alone is not enough to explain the pattern. Additional factors likely contribute, such as:

- Job demands and expectations
- Compensation alignment
- Managerial support levels
- Work–life balance
- Overtime distribution

A multi-factor analysis is recommended to understand why employees closest to the workplace experience elevated attrition.

<img src="https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Attrition%20%25%20by%20Distance%20to%20work.png" height="400">

### Gender

Male employees show a slightly higher attrition rate compared to Female and Non-Binary employees.
The differences, however, are relatively small—indicating that gender is not a major driver of attrition relative to other factors like job role, age, commute, or overtime.

<img src="https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Attrition%20%25%20by%20Gender.png" height="400">

### Job Role

Attrition varies sharply by job category:

- Sales-related roles (Sales Representative, Sales Executive) show the highest attrition, consistent with high-pressure, target-driven environments.
- Recruiters also experience elevated turnover due to rapid workload cycles and market fluctuations.
- Data Scientists show moderate attrition, matching industry norms where job switching is common due to strong demand and competitive pay.
- Technical roles such as Software Engineers, Machine Learning Engineers, and Senior Software Engineers show lower attrition, suggesting greater job stability and clearer career progression.

<img src="https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Attrition%20%25%20by%20Job%20Role.png" height="400">

### Marital Status

Employees who are Single exhibit the highest attrition, nearly twice that of Married and Divorced employees.
Married and Divorced groups show stronger stability, aligning with broader retention trends associated with life stage, mobility, and personal responsibilities.

<img src="https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Attrition%20%25%20by%20Marital%20Status.png" height="400">

### Overtime

Overtime is one of the strongest predictors of attrition.
Employees who work overtime have an attrition rate nearly three times higher than those who do not.

This pattern is systemic across demographics and job roles, and is typically driven by:

- Burnout and fatigue
- Work–life imbalance
- Elevated workload or staffing gaps
- Lower satisfaction in high-demand environments

Reducing overtime or redistributing workload could significantly improve retention.

<img src="https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Attrition%20%25%20by%20Marital%20Status.png" height="400">

### Salary Group

Attrition decreases steadily as salary increases:
Employees earning ₹0–50K have the highest attrition—more than double the rate of the highest salary group.

Attrition declines across each salary tier, reaching its lowest among employees earning ₹300K+.

This suggests:

- Salary is a major attrition driver for early-career or lower-paid employees.
- Competitive compensation strategies and salary benchmarking can significantly reduce turnover.
- Higher salary bands maintain stronger retention due to greater job satisfaction, stability, and experience.

<img src="https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Attrition%20%25%20by%20Salary.png" height="400">

### State

Geographical variation is modest but meaningful:
- California shows the highest attrition, indicating a more competitive and mobile job market.
- Illinois sits at a moderate level.
- New York shows the lowest attrition, reflecting comparatively stronger retention.

Differences may stem from local job markets, cost of living, role distribution, and availability of career opportunities.

<img src="https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Attrition%20%25%20by%20State.png" height="400">

### Stock Option Level

Attrition increases with stock option level—opposite of typical expectations.
Employees with Level 3 stock options leave at over 3× the rate of Level 0 employees.
This suggests stock options may not be perceived as valuable or motivating, possibly due to slow vesting schedules or higher external opportunities for these roles.

<img src="https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Attrition%20%25%20by%20Stock%20Option.png" height="400">

### Travel Needs

Frequent travel can lead to fatigue, reduced work–life balance, and dissatisfaction, all contributing to higher turnover.
Employees with no travel obligations show the strongest retention.

<img src="https://github.com/GH-AkshyM/HR-Attrition-Analytics-Dashboard/blob/main/Screenshots/Attrition%20%25%20by%20Travel%20Needs.png" height="400">

[(Back to top)](#table-of-contents)

## 🛠Recommendations

Traditional HR analytics often relies on comparing multiple variables in isolation—for example, evaluating attrition separately by age, salary band, travel needs, overtime, and so on. While useful, this approach requires continuous manual cross-checking by analysts and HR teams to identify high-risk groups.

**A far more elegant and scalable solution emerges from the integrated insights in this report.**

### Implement a Unified “Attrition Risk Band” System:

Instead of analyzing individual variables one by one, HR should adopt a multi-dimensional risk band framework that consolidates all high-risk attributes into a single, easy-to-interpret structure.

This framework gives HR a benchmark-wide, eagle-eye view of attrition drivers and lets them instantly identify employees who fall into any or multiple high-risk clusters.

#### 🔍 Why This Is Superior (and Future-Proof for 2025)

**No more manual cross-tab analysis:**
Instead of checking age + salary + overtime + role separately, HR can immediately see whether an employee belongs to one or several risk bands.

**Captures compounding risk:**
An employee who is,
- 26–35
- In the ₹0–50K band
- Working overtime
- In a frequent-travel role

is at exponentially elevated risk—not because of one variable, but because of the stacked effect.

**Brings enterprise-level maturity:**
This approach mirrors modern People Analytics teams in top companies who manage attrition proactively through risk scoring models rather than static descriptive charts.

**Scalable and reusable:**
As new factors emerge (remote work, AI skill mismatches, role digitization), they can be added to the risk band system without restructuring the analysis.

**Operationally simple for HR teams:**
They only need to answer one question:

### “Does this employee fall into one or more high-risk bands?”

If yes ➤ flag early ➤ intervene with precision.

#### 🚀 Outcome: A System That Predicts, Not Just Describes

[(Back to top)](#table-of-contents)

