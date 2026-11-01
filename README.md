# HealthConnect Rwanda – Healthcare Analytics & Business Intelligence Project.

## 1. Project Overview

The **HealthConnect Rwanda Healthcare Analytics & Business Intelligence Project** is an end-to-end healthcare data analytics solution developed to evaluate healthcare operations, clinical outcomes, patient demographics, financial performance, and service satisfaction across healthcare facilities in Rwanda.

The project focuses on transforming healthcare datasets into meaningful business intelligence through data preparation, relational data modelling, KPI development, interactive Power BI dashboards, and analytical testing.

The solution is designed to support healthcare management in understanding operational performance, identifying reporting gaps, monitoring financial indicators, and making evidence-based decisions.

## 2. Project Objectives

The main objectives are to:

- Analyse healthcare operations and appointment activity.
- Evaluate patient demographics and clinical diagnosis patterns.
- Monitor financial performance, billing, and payment collection.
- Examine healthcare service delivery and patient satisfaction.
- Develop an integrated Power BI executive dashboard suite.
- Establish a structured analytical data model.
- Validate KPIs, calculations, relationships, and dashboard outputs.
- Identify data quality and reconciliation limitations requiring further investigation.

## 3. Project Scope and Dataset Overview

The project involved healthcare datasets covering different operational and analytical areas.

Key data coverage includes:

| Dataset / Area | Records or Coverage |
|---|---:|
| Patient Profiles | 20,000 |
| Appointments | 5,000 |
| Diagnosis Records | 60,000 |
| Healthcare Facilities | 20 |
| Medical Equipment | 4,000 records |
| Bed Records | 2,000 records |

The datasets support analysis of patient demographics, appointments, diagnoses, departments, facilities, billing, payments, and other healthcare operations.

## 4. Week 6 – Executive Dashboard Suite & System Integration Review

Week 6 focused on developing the HealthConnect Rwanda executive dashboard suite and establishing the analytical data model.

### Key Activities

- Imported and reviewed relevant healthcare datasets.
- Prepared and structured data for Power BI analysis.
- Developed a relational analytical model using a star schema approach.
- Created DAX measures for healthcare KPIs.
- Designed a six-page executive dashboard suite.
- Developed visualisations covering operational, clinical, demographic, financial, and service-related indicators.
- Reviewed system integration and data relationships.

### Dashboard Coverage

The six-page dashboard suite was designed to cover:

1. Healthcare Operations and Appointments.
2. Clinical Outcomes and Diagnosis Analysis.
3. Patient Demographics.
4. Financial Performance and Billing.
5. Patient Satisfaction and Feedback.
6. Executive Overview and Performance Monitoring.

### Key Analytical Highlights

- Patient demographic analysis covered 20,000 patient profiles.
- Appointment analysis covered 5,000 appointment records.
- Diagnosis analysis covered approximately 60,000 diagnosis records.
- Total billed revenue was approximately RWF 9.31 billion.
- Total collected revenue was approximately RWF 8.39 billion.
- Revenue collection rate was approximately 90.1%.
- The diagnosis analysis identified gastritis, diabetes, hypertension, malaria, and upper respiratory infections among the major diagnosis categories.

## 5. Week 7 – Analytics Testing, KPI Validation & Dashboard Refinement

Week 7 focused on testing the analytical outputs developed during Week 6 and documenting findings that could affect reporting accuracy and interpretation.

### Key Activities

- Reviewed KPI calculations and dashboard outputs.
- Examined appointment and billing record matching.
- Investigated revenue allocation and reconciliation differences.
- Reviewed data quality and blank-value handling.
- Examined star schema relationships and department filtering.
- Tested dashboard filters and interactions.
- Captured screenshots and organised supporting evidence.
- Documented outstanding findings for further investigation.

### Key Testing Findings

| Testing Area | Observed Result |
|---|---:|
| Total Appointments | 5,000 |
| Billing Appointment Records | Approximately 60,000 |
| Unique Unmatched AppointmentIDs | Approximately 55,000 |
| Department Allocated Revenue | RWF 771.13 million |
| Unmatched Billing Revenue | Approximately RWF 8.54 billion |
| Revenue_Summary | Approximately RWF 1.13 billion |
| HC_Billing Revenue | Approximately RWF 9.31 billion |
| Revenue Reconciliation Measure | Displayed 0 difference |

These findings highlight differences in record matching, revenue allocation, and reconciliation that require further investigation.

The approximately RWF 8.54 billion associated with unmatched records is not classified as lost revenue or unpaid revenue. It represents billing revenue that has not been matched through the appointment-record matching process.

The displayed zero reconciliation difference should also not be interpreted as proof that all revenue sources have been reconciled.

### Outstanding Findings

The following matters remain documented:

- Unmatched AppointmentIDs between appointment and billing records.
- Billing revenue that has not been allocated through appointment matching.
- Differences between Revenue_Summary and HC_Billing totals.
- Blank results during department-level filtering.
- The interpretation and calculation scope of the revenue reconciliation measure.
- Outstanding balance and payment-status inconsistencies.

These findings have been retained for further guidance and investigation rather than being presented as resolved issues.

## 6. Data Modelling and Analytical Approach

The project uses a structured analytical modelling approach to organise healthcare data and support reporting across different business areas.

The intended model includes transactional fact tables and supporting dimension tables.

Key modelling considerations include:

- Defining primary and foreign keys.
- Establishing appropriate relationships.
- Supporting dimension-to-fact filtering.
- Reviewing relationship cardinality and filter direction.
- Validating matching keys across datasets.
- Avoiding unsupported assumptions when interpreting incomplete or unmatched records.

The model and its relationships were reviewed during Week 7, with some filtering and matching issues retained for further investigation.

## 7. Tools and Technologies

| Tool / Technology | Application |
|---|---|
| Microsoft Power BI | Dashboard development and visual analytics |
| DAX | KPI calculations and analytical measures |
| Microsoft Excel | Data inspection and preparation |
| Data Modelling | Relational modelling and relationship design |
| GitHub | Version control and project documentation |

## 8. Project Deliverables

The combined Week 6 and Week 7 project work includes:

- Six-page executive Power BI dashboard suite.
- Healthcare analytical data model.
- KPI definitions and DAX measures.
- Healthcare operational and financial analysis.
- Executive dashboard review documentation.
- KPI validation documentation.
- Testing and validation records.
- Testing activity tracker.
- Evidence log and supporting screenshots.
- Documented data quality and reconciliation findings.

## 9. Project Limitations

The interpretation of the results is subject to the available datasets and their relationships.

Some limitations identified during the project include:

- Unmatched appointment identifiers across datasets.
- Inconsistent revenue totals between certain financial sources.
- Limited facility and department identifier coverage.
- Incomplete information for validating some operational measures.
- Payment and billing status inconsistencies.
- Department-filtering behaviour requiring further review.

These limitations are documented to support transparent reporting and prevent unsupported conclusions.

## 10. Project Progress

| Project Stage | Focus | Status |
|---|---|---|
| Week 6 | Executive Dashboard Suite & System Integration Review | Completed |
| Week 7 | Analytics Testing, KPI Validation & Dashboard Refinement | Completed |
| Week 8 | Final Integration and Project Readiness | Upcoming |

## 11. Conclusion

The HealthConnect Rwanda project demonstrates the application of data analytics and business intelligence techniques to healthcare operations and management reporting.

Through Week 6, the project established an executive dashboard suite and analytical data model. Week 7 extended this work through KPI review, analytical testing, revenue reconciliation investigation, data quality assessment, and dashboard testing.

Together, these stages provide a structured foundation for the remaining project integration and final readiness activities.

**Current Project Status:** Week 6 and Week 7 completed. Outstanding analytical findings documented for further guidance during Week 8.
