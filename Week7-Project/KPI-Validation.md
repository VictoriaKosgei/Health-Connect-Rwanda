# HealthConnect Rwanda – Week 7 KPI Validation Record

**Project:** HealthConnect Rwanda Healthcare Analytics & Business Intelligence  
**Program:** AnalystLab Africa Internship – Data Analytics Track  
**Phase:** Week 7 – Testing, Validation and Refinement  
**Prepared by:** Victoria Kosgei  
**Reporting Period:** October–November 2026

---

## 1. Purpose of KPI Validation

The purpose of this validation exercise was to review the HealthConnect Rwanda Power BI dashboard and verify that its key performance indicators (KPIs), calculations, and analytical outputs accurately represent the underlying datasets.

The validation focused on:

- Comparing dashboard values against source data.
- Checking financial calculations and payment summaries.
- Validating patient demographics and appointment categories.
- Reviewing diagnosis and insurance indicators.
- Identifying inconsistencies caused by missing or unmatched records.
- Confirming that the dashboard provides reliable information for management decision-making.

## 2. Financial KPI Validation

| KPI | Validated Result | Validation / Interpretation |
|---|---:|---|
| Gross Billed Revenue | RWF 9.31 billion | Confirmed against `HC_Billing[Amount]`. |
| Payments Collected | RWF 8.39 billion | Confirmed against `HC_Payment[AmountPaid]`. |
| Department Allocated Revenue | RWF 771.13 million | Revenue associated with billing records whose AppointmentIDs match appointment records. |
| Revenue Summary | RWF 1.13 billion | Confirmed dashboard summary value. |
| Outstanding Balance | Approximately RWF 920 million | Difference between gross billed revenue and payments collected. |
| Status-Based Outstanding | RWF 919.95 million | Confirmed using billing status-based calculation. |
| Collection Rate | Approximately 90.1% | Payments collected compared with gross billed revenue. |
| Unallocated Billing Revenue | Approximately RWF 8.54 billion | Billing revenue not allocated through the appointment matching relationship. |
| Billing Revenue Reconciliation | RWF 0 displayed | Dashboard output recorded; this does not independently establish that the financial datasets reconcile. |

### Financial Validation Findings

The gross billed revenue and payments collected measures were checked against their respective source tables and returned the same values as the dashboard.

However, the relationship between `HC_Billing` and `Fact_Appointments` revealed a significant matching issue.

- Total billing records: 60,000.
- Matched billing records: 5,000.
- Unmatched billing records: 55,000.
- Distinct unmatched AppointmentIDs: 1,000.
- Gross billed revenue: RWF 9.31 billion.
- Department Allocated Revenue: approximately RWF 771.13 million.

The Department Allocated Revenue figure represents the portion associated with matched appointments. It should not be interpreted as the full gross billed revenue.

The Revenue Summary value of RWF 1.13 billion was also confirmed as the displayed dashboard result. It is retained as a separate metric and should not be assumed to reconcile with the HC_Billing total.

## 3. Patient Demographic KPI Validation

| KPI | Validated Result |
|---|---:|
| Total Patient Profiles | 20,000 |
| Male Patients | 10,090 (50.45%) |
| Female Patients | 9,910 (49.55%) |
| Average Patient Age | Approximately 45 years |

### Validation Finding

The patient demographic figures were reviewed and confirmed. The gender distribution is relatively balanced, with male patients representing 50.45% and female patients representing 49.55% of the patient records.

## 4. Appointment Visit-Type Validation

The `Fact_Appointments` dataset contains 5,000 appointment records. The `VisitType` field identifies three appointment categories.

| Visit Type | Appointment Count | Percentage |
|---|---:|---:|
| Emergency | 1,650 | 33.00% |
| Follow-up | 1,694 | 33.88% |
| Consultation | 1,656 | 33.12% |
| **Total** | **5,000** | **100%** |

### Validation Finding

The three visit-type categories account for all 5,000 appointment records.

Follow-up appointments represent the largest category at 33.88%, followed by Consultation at 33.12% and Emergency at 33.00%.

These categories describe the type of healthcare visit. They do not indicate whether a patient attended, missed, or cancelled an appointment.

## 5. Diagnosis and Chronic Condition Validation

### Diagnosis Records

The diagnosis dataset contains approximately 60,000 diagnosis records.

| Diagnosis Category | Records | Percentage |
|---|---:|---:|
| Gastritis | 12,208 | 20.3% |
| Diabetes | 12,083 | 20.1% |
| Hypertension | 12,075 | 20.1% |
| Malaria | 11,878 | 19.8% |
| Upper Respiratory Infection | 11,756 | 19.6% |
| **Total** | **60,000** | **100%** |

### Chronic Condition Records

| Chronic Condition | Records |
|---|---:|
| Asthma | 4,996 |
| Hypertension | 4,988 |
| Diabetes | 4,945 |

### Validation Findings

- Diagnosis category relationships were checked.
- Zero orphaned diagnosis categories were identified.
- The diagnosis figures represent diagnosis records, not necessarily unique patients or disease prevalence.
- Chronic condition counts are retained as recorded in the source data.

## 6. Insurance KPI Validation

| KPI | Validated Result |
|---|---:|
| Insurance Claim Approval Rate | 49.98% |

### Validation Finding

The insurance approval rate and related dashboard visual were reviewed and counter-checked. The displayed approval rate was confirmed.

Claim statuses include Pending and blank values. These should not automatically be interpreted as rejected claims.

## 7. Department and Facility Mapping Validation

| Validation Check | Result |
|---|---:|
| Matched DepartmentIDs | 200 |
| Unmatched DepartmentIDs | 0 |
| Blank DepartmentIDs in Fact_Appointments | 0 |
| Facility Mapping | Approximately 5% |

### Validation Findings

All 200 department identifiers in the appointment records matched the department reference data.

Facility mapping remains limited, at approximately 5%. Therefore, facility-level comparisons and conclusions should be interpreted cautiously.

## 8. Overall KPI Validation Summary

The KPI review confirmed the principal financial, demographic, appointment visit-type, diagnosis, and insurance values recorded in the dashboard.

The validation also identified limitations in billing-to-appointment matching and facility mapping. These affect the extent to which some financial and facility-level findings can be interpreted.

Attendance and no-show rates are not available because the appointment dataset does not contain an attendance status field.

The validated KPIs are retained for the Week 7 dashboard review, with the identified limitations documented separately.

## 9. Week 8 Considerations

- Improve billing-to-appointment record matching.
- Investigate the difference between the Revenue Summary and HC_Billing totals.
- Improve facility mapping before relying on facility-level comparisons.
- Capture appointment attendance outcomes in future data collection.
- Maintain validation checks when new records and dashboard updates are integrated.

---

**Document Status:** Week 7 KPI validation record – updated with confirmed appointment visit-type counts and documented data limitations.
