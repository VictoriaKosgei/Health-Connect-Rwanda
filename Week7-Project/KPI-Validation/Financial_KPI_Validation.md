# HealthConnect Rwanda – KPI Validation Report
## 1. Purpose

This document records the validation of important HealthConnect Rwanda KPIs against the available datasets and Power BI dashboard outputs.

The objective was to assess calculation accuracy, data consistency, relationships and the reliability of analytical results before final integration.

## 2. Financial KPI Validation

| KPI | Calculation / Definition | Actual Result | Validation Status |
|---|---|---:|---|
| Total Billed Revenue | Sum of billing amounts | RWF 9.31 billion | Reviewed |
| Total Collected Revenue | Sum of recorded payments | RWF 8.39 billion | Reviewed |
| Collection Rate | Collected Revenue ÷ Billed Revenue × 100 | 90.1% | Validated |
| Outstanding Balance | Billed Revenue − Collected Revenue | RWF 920 million | Reviewed |
| Status-Based Outstanding | Sum of outstanding bills based on billing status | RWF 919.95 million | Reconciliation required |
| Department Allocated Revenue | Billing revenue successfully matched to appointments and allocated | RWF 771.13 million | Reviewed |
| Unallocated Billing Revenue | Billing revenue without matching appointment allocation | RWF 8.54 billion | Issue identified |
| Billing Revenue Reconciliation | Reconciled revenue measure displayed in dashboard | RWF 0 | Issue identified |
| Revenue Summary | Revenue reported in Revenue_Summary | RWF 1.13 billion | Discrepancy identified |

### Financial Validation Findings

- Total billing revenue was approximately RWF 9.31 billion.
- Recorded payments amounted to approximately RWF 8.39 billion.
- The calculated collection rate was approximately 90.1%.
- The calculated outstanding balance was approximately RWF 920 million.
- Status-based outstanding bills amounted to RWF 919.95 million, producing a difference of RWF 50,000.
- Department allocated revenue was RWF 771.13 million.
- Approximately RWF 8.54 billion remained unallocated because of unmatched appointment identifiers.
- The Revenue_Summary value of approximately RWF 1.13 billion did not agree with the HC_Billing total.

**Conclusion:** Financial KPIs were reviewed, but complete revenue reconciliation remains outstanding.

## 3. Appointment KPI Validation

| KPI | Definition | Actual Result | Validation Status |
|---|---|---:|---|
| Total Appointments | Count of appointment records | 5,000 | Verified |
| Billing Appointment Count | Count of billing appointment records | 60,000 | Verified |
| Unique Unmatched AppointmentIDs | Count of billing appointment identifiers without matching appointment records | 55,000 | Issue identified |
| Matched Appointment Records | Appointment records successfully linked to billing | Used for revenue allocation | Reviewed |

### Appointment Validation Findings

The appointment dataset contained 5,000 records, while billing contained approximately 60,000 appointment records.

Approximately 55,000 unique AppointmentIDs were unmatched.

This mismatch affected revenue allocation and resulted in blank revenue values when the related appointment records could not be matched through the Power BI model.

**Conclusion:** Appointment counts were verified, but full appointment-to-billing reconciliation remains incomplete.

## 4. Patient and Diagnosis KPI Validation

| KPI | Definition | Actual Result | Validation Status |
|---|---|---:|---|
| Total Patients | Count of patient records | 20,000 | Reviewed |
| Male Patients | Count by recorded gender | 10,090 | Reviewed |
| Female Patients | Count by recorded gender | 9,910 | Reviewed |
| Average Patient Age | Average of recorded patient ages | Approximately 45 years | Reviewed |
| Diagnosis Records | Count of diagnosis transactions | 60,000 | Reviewed |
| Gastritis | Share of diagnosis records | 20.3% | Reviewed |
| Diabetes | Share of diagnosis records | 20.1% | Reviewed |
| Hypertension | Share of diagnosis records | 20.1% | Reviewed |
| Malaria | Share of diagnosis records | 19.8% | Reviewed |
| Upper Respiratory Infection | Share of diagnosis records | 19.6% | Reviewed |

**Conclusion:** Patient demographics and diagnosis distributions were reviewed against the available records. Diagnosis categories were also checked following the data-model corrections.

## 5. Emergency and Attendance Analysis

| KPI | Definition | Actual Result | Validation Status |
|---|---|---:|---|
| Emergency Visits | Count of emergency visits | 1,650 | Reviewed |
| Emergency Visit Share | Emergency Visits ÷ 5,000 Appointments × 100 | 33% | Reviewed |
| Attendance | Appointments attended according to recorded status | Dashboard analysis reviewed | Reviewed |
| No-Show Rate | No-show appointments ÷ applicable appointment records × 100 | Dashboard analysis reviewed | Reviewed |

**Validation note:** Attendance and no-show findings were reassessed using the available 5,000 appointment records. The figures should not be interpreted as representing all 60,000 billing records.

## 6. Data Quality and Model Validation

| Validation Area | Finding | Status |
|---|---|---|
| Blank Values | Blank values omitted from relevant analysis during data preparation. | Action applied |
| AppointmentID Matching | Approximately 55,000 unmatched identifiers. | Outstanding |
| Department Relationships | Blank department results persisted when using the Fact_Appointment relationship path. | Outstanding |
| Facility Mapping | Department-to-facility matching was approximately 5%. | Limitation |
| Billing and Payment Consistency | Inconsistencies between billing status and payment records. | Outstanding |
| Insurance Information | Insurer IDs alone do not confirm actual insurance coverage. | Limitation |
| Revenue Summary | Approximately RWF 1.13 billion versus RWF 9.31 billion in HC_Billing. | Outstanding |

## 7. KPI Validation Summary

The Week 7 validation process reviewed the major financial, appointment, patient, diagnosis and emergency indicators.

The main findings were:

1. The financial collection rate was approximately 90.1%.
2. Approximately 55,000 unmatched AppointmentIDs affected revenue allocation.
3. RWF 771.13 million was allocated to matched appointments.
4. Approximately RWF 8.54 billion remained unallocated.
5. Revenue reconciliation displayed zero.
6. Revenue_Summary did not agree with the main billing dataset.
7. A RWF 50,000 difference existed between outstanding balance calculations.
8. Department and facility reporting remained limited by incomplete relationships.

## 8. Outstanding Actions for Week 8

- Reconcile unmatched AppointmentIDs.
- Investigate unallocated billing revenue.
- Investigate the Revenue_Summary discrepancy.
- Resolve blank department results.
- Reconcile outstanding balance calculations.
- Review billing and payment status inconsistencies.
- Revalidate financial KPIs after integration.
- Confirm that dashboard values agree with the reconciled datasets.

## 9. Final Conclusion

Week 7 KPI validation strengthened confidence in the HealthConnect Rwanda analytical solution by reviewing important calculations, dashboard outputs and underlying data relationships.

Although the dashboard functionality was tested and major KPIs were reviewed, financial reconciliation and appointment matching remain important outstanding issues.

These findings will guide Week 8 integration, further validation and final project readiness.
