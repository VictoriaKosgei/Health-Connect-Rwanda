# HealthConnect Rwanda — Week 8 Final Integration & Project Showcase

## Improving Patient Appointment Attendance and Healthcare Support Using Data and AI

**Programme:** AnalystLab Africa Experience Lab  
**Track:** Data Analytics  
**Week:** 8 — Final Integration and Project Showcase  
**Project:** HealthConnect Rwanda Clinic Experience Lab 

---

## 1. Project Overview

The HealthConnect Rwanda project is a healthcare analytics and business intelligence solution developed to support evidence-based decision-making across healthcare facilities.

The project focuses on evaluating healthcare operations, patient demographics, clinical outcomes, financial performance, and patient experience through data analysis and interactive Power BI dashboards.

Week 8 represents the final integration and presentation stage of the project. The work consolidates the dashboard, KPI validation, analytical findings, testing outcomes, business recommendations, and documented limitations into a final analytics package.

The project also considers how data and AI can support healthcare decision-making while emphasizing the importance of data quality, model validation, and responsible use.

## 2. Week 8 Objectives

The key objectives for Week 8 were to:

- Consolidate the HealthConnect Rwanda analytics deliverables.
- Review the final dashboard and KPI definitions.
- Summarize validated business insights and recommendations.
- Document data quality issues and analytical limitations.
- Prepare the final project presentation.
- Organize supporting evidence and project documentation.
- Present the project’s business value and readiness for further development.

## 3. Project Scope

The project covers the following healthcare data:

| Data Area | Scope |
|---|---:|
| Patient Profiles | 20,000 |
| Appointments | 5,000 |
| Healthcare Facilities | 20 |
| Diagnosis Records | Approximately 60,000 |
| Dashboard Pages | 6 |

The analysis covers patient demographics, appointment activity, diagnoses, financial performance, operational indicators, and patient experience.

## 4. Tools and Technologies

- **Power BI:** Interactive dashboards, data modeling, visual analytics, and KPI reporting.
- **SQL:** Data querying, validation, and analytical preparation.
- **Python:** Data analysis and quality checks.
- **Excel:** Data inspection and supporting validation.
- **GitHub:** Version control, documentation, and project presentation.
- **Markdown:** README files, validation reports, and project documentation.

## 5. Final Dashboard

The HealthConnect Rwanda Power BI dashboard contains six analytical pages.

### Page 1 — Executive Overview
Provides a high-level summary of healthcare activity and key performance indicators.

### Page 2 — Clinical Outcomes
Explores diagnosis records and clinical patterns.

### Page 3 — Patient Demographics
Analyzes patient characteristics, including age and gender.

### Page 4 — Financial Performance
Examines billing, payments, collections, outstanding balances, and insurance-related indicators.

### Page 5 — Operational Performance
Reviews staff distribution, bed availability, equipment availability, and operational comparisons.

### Page 6 — Patient Experience
Presents patient feedback, satisfaction ratings, and complaint-related analysis.

### Dashboard Screenshots

Add screenshots of the final dashboard pages to the `Images/` folder and update the image paths below.

```markdown
![Executive Overview](Images/Executive_Overview.png)

![Clinical Outcomes](Images/Clinical_Outcomes.png)

![Patient Demographics](Images/Patient_Demographics.png)

![Financial Performance](Images/Financial_Performance.png)

![Operational Performance](Images/Operational_Performance.png)

![Patient Experience](Images/Patient_Experience.png)
```

## 6. Key Validated KPIs

The following figures summarize the validated project findings.

| KPI | Validated Result |
|---|---:|
| Patient Profiles | 20,000 |
| Appointments | 5,000 |
| Male Patients | 10,090 — 50.45% |
| Female Patients | 9,910 — 49.55% |
| Average Patient Age | Approximately 45 years |
| Total Billing | Approximately RWF 9.31 billion |
| Total Payments | Approximately RWF 8.39 billion |
| Collection Rate | Approximately 90.1% |
| Outstanding Balance | Approximately RWF 919.95 million |
| Department Allocated Revenue | Approximately RWF 771.13 million |

**Important:** These KPIs should be interpreted alongside the validation findings and data limitations documented in the project.

## 7. Key Business Insights

### Patient Demographics
The patient dataset contains 20,000 profiles. Male patients represent 50.45% of the recorded population, while female patients represent 49.55%.

### Clinical Outcomes
The diagnosis data contains approximately 60,000 records. Gastritis, diabetes, and hypertension are among the most frequently recorded diagnoses.

Diagnosis counts represent recorded diagnosis entries and should not be interpreted as unique patient prevalence.

### Financial Performance
The project records approximately RWF 9.31 billion in billing and RWF 8.39 billion in payments, producing an approximate collection rate of 90.1%.

However, billing-to-appointment mapping limitations affect the reliability of department-level revenue allocation.

### Operational Performance
The available data supports analysis of staff distribution, bed availability, and equipment availability.

Actual bed occupancy and equipment utilization cannot be established reliably because the required historical usage, downtime, and maintenance data are not available.

### Patient Experience
The dashboard provides a framework for reviewing patient feedback and satisfaction. The interpretation of patient experience indicators depends on the completeness and coverage of the available feedback records.

## 8. Data Quality and Validation

Data quality and KPI validation were important components of the final integration process.

The validation work included:

- Reviewing dataset structure and completeness.
- Checking key relationships and appointment identifiers.
- Reviewing KPI definitions and calculations.
- Testing dashboard filters and interactions.
- Investigating financial reconciliation differences.
- Documenting unsupported or unreliable indicators.
- Separating validated results from assumptions.

### Financial Data Mapping Limitation

The billing dataset contains appointment identifiers that do not all match the appointment fact table.

This affects the allocation of billing amounts to departments and appointments.

The project therefore distinguishes between:

- Total billing recorded in the billing dataset.
- Payments recorded in the payment dataset.
- Department Allocated Revenue based on matched records.
- Unallocated billing amounts requiring further investigation.

Department Allocated Revenue should not be interpreted as the complete financial performance of each department.

## 9. Dashboard Testing

The final dashboard was reviewed for usability and analytical consistency.

Testing included:

- Date slicer functionality.
- Department filter functionality.
- Gender filter functionality.
- KPI responsiveness to slicer selections.
- Cross-filtering between visuals.
- Navigation between dashboard pages.
- Reset-filter functionality.
- Review of KPI values against validation results.

The reported dashboard interaction checks passed. Financial mapping limitations remain documented and are not considered resolved merely because the dashboard visuals respond correctly.

## 10. AI and Cross-Track Integration Considerations

The project considered the use of AI for healthcare support and appointment-related analysis.

Model evaluation findings indicated that the emergency-case appointment model
