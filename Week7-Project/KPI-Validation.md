# HealthConnect Rwanda – KPI Validation Report

## 1. Purpose

This document records the validation and review of key HealthConnect Rwanda performance indicators against the available datasets and Power BI dashboard outputs.

The objective was to assess KPI calculation accuracy, data consistency, model relationships and the reliability of analytical results before final project integration.

The validation covered financial performance, appointments, patient demographics, diagnosis records, emergency visits, data quality and dashboard outputs.

## 2. Financial KPI Validation

| KPI | Calculation / Definition | Actual Result | Validation Status |
|---|---|---:|---|
| Total Billed Revenue | Sum of HC_Billing amounts | RWF 9.31 billion | Recalculated and matched |
| Total Collected Revenue | Sum of HC_Payment amounts | RWF 8.39 billion | Recalculated and matched |
| Collection Rate | Collected Revenue ÷ Billed Revenue × 100 | 90.1% | Calculation reviewed |
| Outstanding Balance | Billed Revenue − Collected Revenue | Approximately RWF 920 million | Reviewed |
| Status-Based Outstanding | Sum of outstanding bills based on billing status | RWF 919.95 million | Reconciliation required |
| Department Allocated Revenue | Billing revenue associated with matched appointment records and allocated to departments | RWF 771.13 million | Reviewed |
| Unallocated Billing Revenue | Billing revenue without successful appointment allocation | Approximately RWF 8.54 billion | Issue identified |
| Billing Revenue Reconciliation | Reconciliation measure displayed in the dashboard | RWF 0 | Requires investigation |
| Revenue Summary | Revenue reported in Revenue_Summary | Approximately RWF 1.13 billion | Discrepancy identified |

### 2.1 Financial Validation Findings

- Total billed revenue was approximately RWF 9.31 billion.
- Recorded payments amounted to approximately RWF 8.39 billion.
- The calculated collection rate was approximately 90.1%.
- The calculated outstanding balance was approximately RWF 920 million.
- Status-based outstanding bills amounted to RWF 919.95 million.
- The difference between the two outstanding balance calculations was approximately RWF 50,000.
- Department allocated revenue was approximately RWF 771.13 million.
- Approximately RWF 8.54 billion remained unallocated because of unmatched appointment identifiers.
- The Revenue_Summary value of approximately RWF 1.13 billion did not agree with the HC_Billing total.
- The dashboard reconciliation measure displayed RWF 0, but this result requires further investigation before it can be treated as evidence of successful reconciliation.

### 2.2 Financial Interpretation

The financial results represent different levels of analysis:

- **Total Billed Revenue:** All recorded billing amounts.
- **Total Collected Revenue:** All recorded payment amounts.
- **Department Allocated Revenue:** Billing revenue successfully associated with matched appointment records and allocated to departments.
- **Unallocated Billing Revenue:** Billing revenue that could not be allocated through the available appointment relationship.

The difference between gross billed revenue and department allocated revenue is therefore an important data-model and reconciliation limitation.

**Conclusion:** Gross billed revenue and payments collected were independently recalculated and matched the dashboard values. Other financial measures were reviewed, but complete financial reconciliation remains outstanding.

## 3. Appointment KPI Validation

| KPI | Definition | Actual Result | Validation Status |
|---|---|---:|---|
| Total Appointments | Count of records in Fact_Appointments | 5,000 | Verified |
| Billing Records | Count of records in HC_Billing | 60,000 | Verified |
| Appointment IDs in Fact_Appointments | Distinct appointment identifiers in the appointment dataset | 5,000 | Verified |
| Matched Appointment IDs | Appointment identifiers successfully matched between the datasets | 5,000 | Reviewed |
| Unmatched Billing Records | Billing records associated with appointment identifiers absent from Fact_Appointments | 55,000 | Issue identified |
| Distinct Unmatched Appointment IDs | Unique unmatched identifiers in the billing dataset | 1,000 | Issue identified |

### 3.1 Appointment Validation Findings

The appointment dataset contained 5,000 records, while the billing dataset contained 60,000 records.

All 5,000 appointment identifiers in Fact_Appointments were represented in the matching process.

However, 55,000 billing records were associated with 1,000 distinct appointment identifiers that were not present in Fact_Appointments.

The additional identifiers ranged from 5001 to 6000.

This mismatch affected the relationship between billing and appointment data and contributed to blank department results when billing revenue was analyzed through the appointment relationship.

**Conclusion:** Appointment identifiers and their matching results were reviewed. Full billing-to-appointment reconciliation remains incomplete.

## 4. Patient Demographic and Diagnosis KPI Validation

### 4.1 Patient Demographics

| KPI | Definition | Actual Result | Validation Status |
|---|---|---:|---|
| Total Patients | Count of patient records | 20,000 | Reviewed |
| Male Patients | Count of records with Male gender | 10,090 | Reviewed |
| Female Patients | Count of records with Female gender | 9,910 | Reviewed |
| Male Patient Share | Male patients ÷ total patients × 100 | 50.45% | Counter-checked |
| Female Patient Share | Female patients ÷ total patients × 100 | 49.55% | Counter-checked |
| Average Patient Age | Average of recorded patient ages | Approximately 45 years | Reviewed |

The gender distribution was corrected and counter-checked:

- Male: 50.45%.
- Female: 49.55%.

### 4.2 Diagnosis Distribution

The diagnosis dataset contained approximately 60,000 diagnosis records.

| Diagnosis | Diagnosis Records | Share of Diagnosis Records |
|---|---:|---:|
| Gastritis | 12,208 | 20.3% |
| Diabetes | 12,083 | 20.1% |
| Hypertension | 12,075 | 20.1% |
| Malaria | 11,878 | 19.8% |
| Upper Respiratory Infection | 11,756 | 19.6% |

### 4.3 Chronic Condition Records

| Chronic Condition | Records |
|---|---:|
| Asthma | 4,996 |
| Hypertension | 4,988 |
| Diabetes | 4,945 |

### 4.4 Interpretation

The diagnosis figures represent diagnosis records rather than necessarily representing unique patients or disease prevalence.

The diagnosis categories were reviewed following the data-model validation work.

**Conclusion:** Patient demographics and diagnosis distributions were reviewed against the available records. The findings should be interpreted within the limits of the available data.

## 5. Emergency and Attendance Analysis

| KPI | Definition | Actual Result | Validation Status |
|---|---|---:|---|
| Emergency Visits | Count of appointments classified as Emergency | 1,650 | Reviewed |
| Emergency Visit Share | Emergency visits ÷ 5,000 appointments × 100 | 33% | Calculation reviewed |
| Attendance | Appointments attended according to recorded status | Pending final confirmation | Outstanding |
| No-Show Rate | No-show appointments ÷ applicable appointment records × 100 | Pending final confirmation | Outstanding |

### 5.1 Validation Notes

Emergency visits are based on appointment type.

Appointment types such as Follow-up, Consultation and Emergency must not be confused with attendance outcomes.

Attendance and no-show calculations require confirmation using the actual appointment status values and underlying records in Fact_Appointments.

The appropriate appointment population for these calculations is the 5,000 appointment records, not the 60,000 billing records.

**Conclusion:** Emergency visit analysis was reviewed. Attendance and no-show validation remains outstanding until the underlying status values and calculations are confirmed.

## 6. Data Quality and Model Validation

| Validation Area | Finding | Status |
|---|---|---|
| Blank Values | Blank values were omitted from relevant analysis during data preparation | Action applied |
| Appointment
