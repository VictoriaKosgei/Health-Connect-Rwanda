# HealthConnect Rwanda – Healthcare Analytics & Business Intelligence Project

## Project Overview

HealthConnect Rwanda is a healthcare analytics and business intelligence project developed as part of the AnalystLab Africa Data Analytics Internship.

The project focuses on transforming healthcare operational, clinical, demographic, and financial data into meaningful insights through data preparation, relational data modelling, KPI development, and interactive Power BI dashboards.

The solution was developed to support healthcare management by improving visibility into patient demographics, appointment patterns, clinical diagnoses, financial performance, insurance claims, and healthcare operations.

The project progressed through two major phases:

- **Week 6 – Dashboard Development and System Integration Review**
- **Week 7 – Testing, KPI Validation and Refinement**

## Project Information

| Item | Description |
|---|---|
| Project Name | HealthConnect Rwanda |
| Internship | AnalystLab Africa |
| Track | Data Analytics |
| Project Period | October–November 2026 |
| Primary Tool | Microsoft Power BI |
| Supporting Tools | DAX, Excel, SQL, Python, GitHub |
| Healthcare Facilities | 20 |
| Patient Profiles | 20,000 |
| Appointment Records | 5,000 |
| Dashboard Pages | 6 |

## Business Problem

Healthcare organizations generate large volumes of clinical, operational, patient, and financial data. However, fragmented information and inconsistent relationships can make it difficult for management to obtain a complete view of healthcare performance.

HealthConnect Rwanda addresses this challenge through an integrated analytics solution designed to:

- Improve visibility into patient demographics and clinical records.
- Monitor appointment and healthcare service patterns.
- Analyse financial billing and payment performance.
- Review insurance claim indicators.
- Support department and facility-level analysis where data relationships allow.
- Identify data quality and integration weaknesses.
- Provide evidence-based insights for management decisions.

## Project Objectives

1. Prepare and analyse healthcare datasets.
2. Develop a structured relational data model.
3. Build a six-page interactive executive dashboard.
4. Create DAX measures for healthcare performance indicators.
5. Validate dashboard outputs against source datasets.
6. Test interactive functionality and data relationships.
7. Identify analytical limitations and recommend improvements.

# Week 6 – Dashboard Development and System Integration Review

## 1. Data Preparation and Integration

The Week 6 phase focused on preparing healthcare datasets and integrating them into a Power BI analytics environment.

The project included patient profiles, appointments, diagnoses, laboratory tests, prescriptions, admissions, billing, payments, insurance claims, and supporting reference data.

The data model was organized to support analysis across multiple healthcare areas.

## 2. Data Model

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

## 3. Executive Dashboard Development

A six-page interactive Power BI executive dashboard was developed.

The dashboard covers:

1. Executive Overview
2. Clinical Outcomes
3. Patient Demographics
4. Financial Performance
5. Operational Performance
6. Patient Experience

The dashboard incorporates KPI cards, charts, comparisons, slicers, and interactive filtering to support healthcare performance monitoring.

## 4. Week 6 Deliverables

- Data preparation and integration.
- Relational data modelling.
- DAX KPI development.
- Six-page Power BI executive dashboard.
- Dashboard visuals and interactive features.
- Initial analytical review.

# Week 7 – Testing, Validation and Refinement

## 1. Testing and Validation

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

## 2. Key Validated Results

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

### Clinical and Insurance Indicators

- Diagnosis records: approximately 60,000.
- Gastritis: 12,208 records.
- Diabetes: 12,083 records.
- Hypertension: 12,075 records.
- Malaria: 11,878 records.
- Upper Respiratory Infection: 11,756 records.
- Insurance claim approval rate: 49.98%.
- Chronic condition records include asthma, hypertension, and diabetes.

These diagnosis figures represent recorded diagnosis entries rather than unique patients or population-level prevalence.

## 3. Data Quality Findings

| Validation Area | Result |
|---|---:|
| Total Billing Records | 60,000 |
| Matched Billing Records | 5,000 |
| Unmatched Billing Records | 55,000 |
| Distinct Unmatched AppointmentIDs | 1,000 |
| Matched DepartmentIDs | 200 |
| Unmatched DepartmentIDs | 0 |
| Blank Appointment DepartmentIDs | 0 |

The review identified significant billing-to-appointment matching limitations despite successful department identifier matching.

## 4. Dashboard Functionality Testing

The following interactive features were tested successfully:

- Date slicers.
- Department slicers.
- Gender slicers.
- KPI card responsiveness.
- Chart cross-filtering.
- Page navigation.
- Reset and clear filters.

The tested interactions passed the Week 7 functionality review.

## 5. Cross-Track Testing Contribution

The Data Science track reported testing an appointment-related emergency prediction model using hold-out testing, label-shuffle testing, time-based validation, calibration, and segment checks.

The reported results showed weak performance on unseen data, with approximately 0.50 AUC. The model did not meet its release criteria.

The findings highlighted target-label and underlying data limitations, including missing admissions and attendance information and broken table links.

The recommendation was to avoid deployment until the data and target definition were improved.

These results are recorded as Data Science track testing findings relevant to the overall HealthConnect solution.

# Key Data Limitations

The Week 7 validation identified several issues requiring attention:

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

### Important Appointment Data Clarification

The appointment dataset contains three `VisitType` categories: Emergency, Follow-up, and Consultation.

These represent appointment types, not attendance outcomes.

Attendance Rate and No-Show Rate cannot be calculated because the dataset does not contain an attendance status field.

# Tools and Technologies

| Technology | Application |
|---|---|
| Microsoft Power BI | Dashboard development and visualization |
| DAX | KPI calculations and analytical measures |
| Excel | Data inspection and validation |
| SQL | Data querying and analysis |
| Python | Data analysis and validation support |
| GitHub | Version control and project documentation |

# Project Structure

```text
HealthConnect_Rwanda/
│
├── Week6_Dashboard_Development/
│   ├── Data/
│   ├── PowerBI/
│   ├── Reports/
│   ├── Presentations/
│   ├── Screenshots/
│   └── README.md
│
├── Week7_Testing_Validation_Refinement/
│   ├── 01_Testing_Plan/
│   ├── 02_KPI_Validation/
│   ├── 03_Data_Quality_Validation/
│   ├── 04_Dashboard_Testing/
│   ├── 05_Analytical_Validation/
│   ├── 06_Cross_Track_Collaboration/
│   ├── 07_Refinement_Evidence/
│   ├── 08_Screenshots_Evidence/
│   └── README.md
│
└── README.md
```

*Folder names and file placement should reflect the actual files committed to the repository.*

# Overall Project Outcomes

Across Weeks 6 and 7, the project delivered:

- A structured healthcare analytics data model.
- A six-page interactive Power BI executive dashboard.
- Healthcare performance KPIs and analytical measures.
- Financial, demographic, clinical, and appointment analysis.
- KPI validation against underlying source datasets.
- Data relationship and quality testing.
- Dashboard interaction testing.
- Cross-track testing findings from the Data Science track.
- Documented data limitations and recommendations for further integration.

# Conclusion

HealthConnect Rwanda demonstrates how healthcare data can be transformed into an interactive business intelligence solution for monitoring healthcare operations, patient demographics, clinical records, and financial performance.

Week 6 established the dashboard and analytics foundation, while Week 7 focused on testing, validation, and identifying areas requiring further refinement.

The project provides a documented foundation for continued integration and final project preparation in Week 8.

---

**Project:** HealthConnect Rwanda  
**Program:** AnalystLab Africa Internship  
**Track:** Data Analytics  
**Development Phase:** Weeks 6–7  
**Current Status:** Dashboard development, testing, and validation documented; identified data limitations remain subject to further integration and review.
