# HR Attrition Analytics Dashboard

## ↪️Project background:
This dataset is one of the most widely used HR analytics datasets.  
I wanted to put **my own spin** on it by creating a **clean, clutter-free dashboard** that delivers **maximum insight with minimum noise**.  

I also implemented a modern ETL approach using **Dataflow Gen2**, which acts as the data preparation pipeline before the model loads into Power BI.  
(Scroll down to learn more.)

Thanks for stopping by — hope you enjoy the project!
## 📚Table of Contents:
[Dashboard Video Demo](#dashboard-video-demo)
|**No.**  |**Section**|
|:-: | :------------ | 
|1.   |  [Business Problem](#business-problem)                              |
|2.   |  [Existing Environment](#existing-environment)                              |
|3.   |  [Technical Requirements](#technical-requirements)                              |
|4.   |  [Highlight Features](#highlight-features)                              |
|5.   |  [Future scope of the Dashboard](#future-scope-of-the-dashboard)                              |
## 🎯 Project Objective & What It Solves
This project focuses on understanding **why employees leave** and identifying **which segments are most at risk** using a clean, high-information HR Attrition dashboard.

The analysis helps HR answer:
- What is the overall attrition rate?
- Which departments, job roles, or age groups face the highest turnover?
- How do salary, tenure, overtime, and satisfaction influence attrition?
- Which employee segments should HR prioritize for retention efforts?

The goal is simple:  
Deliver **maximum insight with minimal clutter**, using field parameters and a Dataflow Gen2 ETL pipeline.

## 🗂 Dataset Overview  
A clean HR dataset containing demographic, job, compensation, and satisfaction variables.  
Key fields include:  
- Age, Gender, Education  
- Department, Job Role, Job Level  
- Monthly Income, Stock Option Level  
- Years at Company, Years in Current Role  
- Job Satisfaction, Work–Life Balance  
- **Attrition (Yes/No)**

The dataset is fully anonymized and safe for public analytics use.

## 📊 Data Pipeline (Dataflow Gen2)  
I used **Microsoft Fabric Dataflow Gen2** as the ETL layer.  
Its purpose in this project:  
- Ingest raw HR data  
- Perform cleaning and type conversions  
- Create derived bands (Age Band, Income Band, Tenure Group)  
- Publish a **single clean table** ready for Power BI modeling  
- Enable easy refresh & governance for enterprise-style workflows  

This design simulates a *real corporate setup* where analysts rely on governed, reusable dataflows.

## 📊 Data Model & Metrics  
A simple, clean model optimized for performance and readability.  
Key metrics include:  
- **Total Employees**  
- **Attrition Count**  
- **Attrition Rate**  
- Attrition by Department, Role, Age Band, Income Band, Tenure, Gender  

Field parameters are used to switch between:  
- Metrics  
- Dimensions  
- Categories  

…without cluttering the canvas.

## 🖥 Dashboard Highlights  
The report focuses on **clarity, readability, and high information density**.

**Features include:**  
- One-page design with no visual overload  
- Smart grouping of demographic, compensation, and job insights  
- Interactive field parameters to flip between different views  
- Clean visuals, light color palette, minimal text  
- Dynamic segmentation to identify high-risk groups

The dashboard is intentionally designed to feel **modern, efficient, and recruiter-friendly**.

## 💡 Insights & Recommendations

### 🔍 Key Insights
- **Mid-career employees (25–35 age band)** show significantly higher attrition, especially in customer-facing and high-pressure roles.
- **Overtime is a major driver** — employees with frequent overtime leave at nearly 2x the rate of those with balanced schedules.
- **Entry-level and mid-level job roles** in Sales and R&D have the highest turnover, indicating capability gaps or workload imbalance.
- Employees with **low Job Satisfaction** or **poor Work–Life Balance** contribute disproportionately to attrition.
- **Lower income bands** show higher attrition, pointing to potential compensation competitiveness issues.
- Employees with **<2 years of tenure** are leaving the fastest, suggesting gaps in onboarding, mentoring, or career clarity.
- High performers (in some roles) also show notable attrition, indicating *burnout*, not just disengagement.

---

### 🛠 Recommendations
- **Targeted Retention for Mid-Career Employees**  
  Offer improved career pathways, rotational programs, and clearer promotion criteria.

- **Introduce Overtime Controls**  
  Audit departments with excessive OT and implement workload balancing or staffing adjustments.

- **Strengthen Onboarding & First-Year Experience**  
  Mentorship programs, structured learning paths, and frequent check-ins for new hires (<2 years).

- **Review Compensation Bands for Key Roles**  
  Benchmark market salaries for Sales, R&D, and job levels with high attrition.

- **Engagement Programs for At-Risk Segments**  
  Focus on departments with low satisfaction scores—run targeted pulse surveys and immediate corrective actions.

- **Promote Work–Life Balance**  
  Encourage flexible shifts, optional remote days, or wellness time-offs in departments with high burnout signals.

- **Retain High Performers Proactively**  
  Provide stretch projects, recognition programs, and periodic career discussions before they disengage.

---

These insights and recommendations tie directly into the dashboard and demonstrate practical business value—not just analytics.


## 🚀Future scope of the Dashboard


