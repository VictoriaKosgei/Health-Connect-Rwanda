# HealthConnect Rwanda – Healthcare Analytics & Business Intelligence Project

## Improving Patient Appointment Attendance and Healthcare Support Using Data and AI

**Programme:** AnalystLab Africa Internship  
**Track:** Data Analytics  
**Project:** HealthConnect Rwanda  
**Project Period:** October–November 2026  
**Project Weeks:** 6, 7 and 8  
**Project Author:** Victoria Kosgei  

---

## 1. Project Overview

HealthConnect Rwanda is a healthcare analytics and business intelligence project developed as part of the AnalystLab Africa Data Analytics Internship.

The project focuses on transforming healthcare operational, clinical, demographic, and financial data into meaningful insights through data preparation, relational data modelling, KPI development, validation, and interactive Power BI dashboards.

The solution was designed to support healthcare management by improving visibility into patient demographics, appointment patterns, clinical diagnoses, financial performance, insurance claims, healthcare operations, and patient experience.

The project progressed through three major phases:

- **Week 6 – Dashboard Development and System Integration Review**
- **Week 7 – Testing, KPI Validation and Refinement**
- **Week 8 – Final Integration, Documentation and Project Showcase**

The three phases established the analytics foundation, tested the reliability of the outputs, and consolidated the final project deliverables.

## 2. Project Scope and Information

| Item | Description |
|---|---|
| Project Name | HealthConnect Rwanda |
| Internship | AnalystLab Africa |
| Track | Data Analytics |
| Project Period | October–November 2026 |
| Healthcare Facilities | 20 |
| Patient Profiles | 20,000 |
| Appointment Records | 5,000 |
| Diagnosis Records | Approximately 60,000 |
| Dashboard Pages | 6 |
| Primary Tool | Microsoft Power BI |
| Supporting Tools | DAX, Excel, SQL, Python, GitHub |

## 3. Business Problem

Healthcare organizations generate large volumes of clinical, operational, patient, and financial data. However, fragmented information, inconsistent identifiers, and incomplete records can make it difficult for management to obtain a reliable view of healthcare performance.

HealthConnect Rwanda addresses this challenge through an integrated analytics solution designed to:

- Improve visibility into patient demographics and clinical records.
- Monitor appointment and healthcare service patterns.
- Analyse financial billing and payment performance.
- Review insurance claim indicators.
- Support department and facility-level analysis where data relationships allow.
- Identify data quality and integration weaknesses.
- Provide evidence-based insights for management decisions.
- Evaluate the reliability of analytics and AI-related outputs.

## 4. Project Objectives

1. Prepare and analyse healthcare datasets.
2. Develop a structured relational data model.
3. Build a six-page interactive executive dashboard.
4. Create DAX measures for healthcare performance indicators.
5. Validate dashboard outputs against source datasets.
6. Test interactive functionality and data relationships.
7. Identify data quality issues and analytical limitations.
8. Develop business insights and recommendations.
9. Document integration findings and prepare the final project presentation.

---

# 5. Week 6 – Dashboard Development and System Integration Review

## 5.1 Data Preparation and Integration

Week 6 focused on preparing healthcare datasets and integrating them into a Power BI analytics environment.

The project included patient profiles, appointments, diagnoses, laboratory tests, prescriptions, admissions, billing, payments, insurance claims, and supporting reference data.

The data model was organized to support analysis across multiple healthcare areas.

## 5.2 Data Model

A relational star-schema-oriented model was developed around the central appointment fact table.

### Main Fact Tables

- `Fact_Appointments`
- `Fact_Diagnoses`
- `Fact_Laboratory_Tests`
- `Fact_Prescriptions`
- `Fact_Admissions`
- `Fact_Billing`
- `Fact_Payments`
- `Fact_InsuranceClaims`

### Dimension and Reference Tables

- `HC_Patients`
- `HC_Departments`
- `HC_Doctor`
- `HC_Nurse`
- `HC_Rooms`
- `HC_Beds`
- `HC_Medical_Equipment`
- `Dim_Calendar`

The model was designed to support healthcare analysis through shared identifiers and appropriate table relationships.

## 5.3 Executive Dashboard Development

A six-page interactive Power BI executive dashboard was developed.

| Page | Dashboard Area | Purpose |
|---|---|---|
| 1 | Executive Overview | High-level healthcare performance indicators |
| 2 | Clinical Outcomes | Diagnosis records and clinical patterns |
| 3 | Patient Demographics | Patient age and gender analysis |
| 4 | Financial Performance | Billing, payments, collections and insurance indicators |
| 5 | Operational Performance | Staff, bed availability, equipment and operational comparisons |
| 6 | Patient Experience | Feedback, satisfaction and complaint analysis |

The dashboard incorporates KPI cards, charts, comparisons, slicers, and interactive filtering to support healthcare performance monitoring.

## 5.4 Week 6 Deliverables

- Data preparation and integration.
- Relational data modelling.
- DAX KPI development.
- Six-page Power BI executive dashboard.
- Dashboard visuals and interactive features.
- Initial analytical review.
- Initial system integration review.

---

# 6. Week 7 – Testing, KPI Validation and Refinement

## 6.1 Testing and Validation

Week 7 focused on verifying the reliability of the Week 6 analytics solution.

The review included:

- KPI calculations and source-data comparisons.
- Data relationship validation.
- Appointment category analysis.
- Patient demographic validation.
- Diagnosis and insurance KPI checks.
- Financial performance validation.
- Interactive dashboard functionality testing.
- Documentation of data limitations.

## 6.2 Key Validated Results

### Financial Performance

| KPI | Result |
|---|---:|
| Gross Billed Revenue | RWF 9.31 billion |
| Payments Collected | RWF 8.39 billion |
| Department Allocated Revenue | RWF 771.13 million |
| Revenue Summary | RWF 1.13 billion |
| Outstanding Balance | Approximately RWF 920 million |
| Collection Rate | Approximately 90.1% |
| Unallocated Billing Revenue | Approximately RWF 8.54 billion |

The financial figures require careful interpretation because billing-to-appointment matching and revenue reconciliation issues remain unresolved.

### Patient Demographics

| KPI | Result |
|---|---:|
| Total Patient Profiles | 20,000 |
| Male Patients | 10,090 (50.45%) |
| Female Patients | 9,910 (49.55%) |
| Average Patient Age | Approximately 45 years |

### Appointment Visit Types

| Visit Type | Count | Percentage |
|---|---:|---:|
| Emergency | 1,650 | 33.00% |
| Follow-up | 1,694 | 33.88% |
| Consultation | 1,656 | 33.12% |
| **Total** | **5,000** | **100%** |

These categories represent appointment visit types, not attendance outcomes.

### Clinical and Insurance Indicators

| Indicator | Result |
|---|---:|
| Diagnosis Records | Approximately 60,000 |
| Gastritis | 12,208 records |
| Diabetes | 12,083 records |
| Hypertension | 12,075 records |
| Malaria | 11,878 records |
| Upper Respiratory Infection | 11,756 records |
| Insurance Claim Approval Rate | 49.98% |

Chronic condition records include asthma, hypertension, and diabetes.

Diagnosis figures represent recorded diagnosis entries rather than unique patients or population-level disease prevalence.

## 6.3 Data Quality Findings

| Validation Area | Result |
|---|---:|
| Total Billing Records | 60,000 |
| Matched Billing Records | 5,000 |
| Unmatched Billing Records | 55,000 |
| Distinct Unmatched Appointment IDs | 1,000 |
| Matched Department IDs | 200 |
| Unmatched Department IDs | 0 |
| Blank Appointment Department IDs | 0 |

The review identified significant billing-to-appointment matching limitations despite successful department identifier matching.

## 6.4 Dashboard Functionality Testing

The following interactive features were tested:

- Date slicers.
- Department slicers.
- Gender slicers.
- KPI card responsiveness.
- Chart cross-filtering.
- Page navigation.
- Reset and clear filters.

The tested interactions passed the Week 7 functionality review.

## 6.5 Cross-Track Testing Contribution

The Data Science track reported testing an appointment-related emergency prediction model using:

- Hold-out testing.
- Label-shuffle testing.
- Time-based validation.
- Calibration review.
- Segment-level checks.
- Threshold review.

The reported results showed weak performance on unseen data, with AUC around 0.50 and validation AUC approximately 0.51, compared with a higher training result of approximately 0.75.

The model did not meet its release criteria and was not recommended for operational deployment.

The findings highlighted target-label and underlying data limitations, including missing admissions and attendance information and broken table links.

These results are documented as Data Science track testing findings relevant to the overall HealthConnect solution.

## 6.6 Week 7 Deliverables

- KPI validation documentation.
- Data quality validation.
- Dashboard functionality testing.
- Analytical validation findings.
- Cross-track testing findings.
- Identified issues and limitations.
- Dashboard refinement evidence.
- Updated project documentation.

---

# 7. Week 8 – Final Integration and Project Showcase

## 7.1 Week 8 Objectives

Week 8 focused on consolidating the HealthConnect Rwanda project into a final, documented analytics package.

The objectives included:

- Reviewing the completed dashboard.
- Consolidating KPI validation findings.
- Finalizing business insights and recommendations.
- Documenting integration readiness and outstanding limitations.
- Preparing the final PowerPoint presentation.
- Organizing supporting evidence and documentation.
- Communicating the project's business value and future improvement requirements.

## 7.2 Final Analytics Package

The Week 8 package brings together the following project components:

| Deliverable | Description |
|---|---|
| Final Power BI Dashboard | Six-page healthcare analytics dashboard |
| Final KPI Summary | Consolidated healthcare performance indicators |
| Executive Summary | High-level project findings |
| Business Insights | Evidence-based analytical observations |
| Business Recommendations | Proposed management actions |
| Integration Readiness | Summary of integration findings and outstanding issues |
| Final Presentation | Project overview, findings, limitations and recommendations |
| Evidence | Dashboard screenshots and supporting validation records |
| README | Consolidated project documentation |

## 7.3 Final Business Insights

### Patient Demographics

The patient dataset contains 20,000 profiles. Male patients represent 50.45% of the recorded population, while female patients represent 49.55%.

The average recorded patient age is approximately 45 years.

### Clinical Outcomes

The diagnosis dataset contains approximately 60,000 records. Gastritis, diabetes, hypertension, malaria, and upper respiratory infections are among the frequently recorded diagnoses.

These figures represent diagnosis entries and should not be interpreted as unique patient counts or population prevalence.

### Financial Performance

The project records approximately RWF 9.31 billion in gross billing and RWF 8.39 billion in payments, producing an approximate collection rate of 90.1%.

However, billing-to-appointment mapping limitations affect the reliability of department-level revenue allocation.

### Operational Performance

The available data supports analysis of staff distribution, bed availability, and equipment availability.

Actual bed occupancy and equipment utilization cannot be established reliably because historical usage, downtime, and maintenance information are unavailable.

### Patient Experience

The dashboard provides a framework for reviewing patient feedback and satisfaction. Interpretation of patient experience indicators depends on the completeness and coverage of the available feedback records.

## 7.4 Business Recommendations

### 1. Improve Data Quality and Integration

Establish consistent appointment, billing, payment, department, and facility identifiers to improve data matching and reporting accuracy.

### 2. Strengthen Financial Reconciliation

Investigate unmatched billing records and reconcile billing, payment, and revenue summary datasets before using department-level financial indicators for management decisions.

### 3. Improve Appointment Attendance Tracking

Capture appointment attendance status, cancellation status, and no-show reasons to support reliable attendance analysis.

### 4. Improve Operational Data Collection

Maintain historical bed occupancy, equipment usage, downtime, and maintenance records to enable actual utilization analysis.

### 5. Improve Patient Experience Monitoring

Increase feedback coverage and establish consistent patient satisfaction and complaint tracking.

### 6. Apply Responsible AI Practices

Do not deploy the evaluated predictive model until it demonstrates reliable performance, passes validation and release gates, and receives appropriate review.

## 7.5 Final Presentation

The final Week 8 presentation summarizes:

1. Project overview.
2. Healthcare business problem.
3. Project objectives.
4. Data scope and sources.
5. Data model and dashboard development.
6. Six-page Power BI dashboard.
7. Key performance indicators.
8. Business insights.
9. Financial validation findings.
10. Dashboard testing.
11. AI evaluation and cross-track findings.
12. Data limitations.
13. Business recommendations.
14. Project conclusion and future improvements.

The presentation is supported by the final analytics documentation and available project evidence.

---

# 8. Key Data Limitations Across the Project

The following limitations remain important when interpreting the project findings.

| Area | Limitation |
|---|---|
| Billing Integration | 55,000 billing records remain unmatched to appointment records. |
| Revenue Reconciliation | Different financial outputs require further investigation. |
| Facility Mapping | Approximately 5% facility mapping limits facility-level analysis. |
| Appointment Attendance | No attendance status field is available. |
| Bed Utilization | No reliable occupancy history. |
| Room Utilization | Insufficient room occupancy information. |
| Equipment Utilization | Insufficient usage and downtime history. |
| Diagnosis Analysis | Diagnosis counts cannot automatically be interpreted as unique patients or prevalence. |
| Insurance Claims | Pending and blank claim statuses require careful interpretation. |
| AI Prediction | The evaluated model did not meet its release criteria. |

### Important Appointment Data Clarification

The appointment dataset contains three `VisitType` categories:

- Emergency
- Follow-up
- Consultation

These represent appointment types, not attendance outcomes.

Attendance Rate and No-Show Rate cannot be calculated reliably because the dataset does not contain an attendance status field.

### Financial Data Mapping Clarification

The billing dataset contains 60,000 records, while only 5,000 billing records matched the appointment fact table in the validation review.

The project therefore distinguishes between:

- Total billing recorded in the billing dataset.
- Payments recorded in the payment dataset.
- Department Allocated Revenue based on matched records.
- Unallocated billing amounts requiring further investigation.
- The separate Revenue Summary output.

Department Allocated Revenue should not be interpreted as the complete financial performance of each department.

---

# 9. Tools and Technologies

| Technology | Application |
|---|---|
| Microsoft Power BI | Dashboard development and visualization |
| DAX | KPI calculations and analytical measures |
| Excel | Data inspection and validation |
| SQL | Data querying and analysis |
| Python | Data analysis and validation support |
| GitHub | Version control and project documentation |
| Markdown | Project documentation and reporting |

---

# 10. Overall Project Outcomes

Across Weeks 6, 7 and 8, the project delivered:

- A structured healthcare analytics data model.
- A six-page interactive Power BI executive dashboard.
- Healthcare performance KPIs and analytical measures.
- Financial, demographic, clinical, and appointment analysis.
- KPI validation against underlying source datasets.
- Data relationship and quality testing.
- Dashboard interaction testing.
- Documented cross-track AI model testing findings.
- Business insights and evidence
