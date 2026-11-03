# HealthConnect Rwanda – Week 7: Testing, Validation & Refinement

## Project Overview

Week 7 focused on systematically testing, validating, and refining the HealthConnect Rwanda Healthcare Analytics and Business Intelligence solution developed during Week 6.

The objective was to verify the reliability of dashboard KPIs, test interactive functionality, validate analytical findings against source datasets, identify data limitations, and document recommendations for further system integration.

This phase focused on improving analytical reliability and ensuring that dashboard outputs could be interpreted appropriately for healthcare management decision-making.

## Project Information

| Item | Description |
|---|---|
| Project | HealthConnect Rwanda |
| Program | AnalystLab Africa Internship |
| Track | Data Analytics |
| Project Phase | Week 7 |
| Tools | Power BI, DAX, Excel, SQL, Python, GitHub |
| Dashboard | Six-page interactive executive dashboard |
| Healthcare Facilities | 20 |
| Patient Profiles | 20,000 |
| Appointment Records | 5,000 |

## Week 7 Objectives

- Review and test Week 6 dashboard outputs.
- Validate KPI calculations against source data.
- Test dashboard filters, navigation, and cross-filtering.
- Investigate unexpected financial and relationship results.
- Validate patient demographics, appointment categories, diagnoses, and insurance indicators.
- Identify data quality and integration limitations.
- Review cross-track testing findings from the Data Science track.
- Document validated findings, limitations, and recommendations.

## 1. KPI Validation

Key dashboard indicators were reviewed and compared against the available source datasets.

### Financial Performance

| KPI | Validated Result |
|---|---:|
| Gross Billed Revenue | RWF 9.31 billion |
| Payments Collected | RWF 8.39 billion |
| Department Allocated Revenue | RWF 771.13 million |
| Revenue Summary | RWF 1.13 billion |
| Outstanding Balance | Approximately RWF 920 million |
| Status-Based Outstanding | RWF 919.95 million |
| Collection Rate | Approximately 90.1% |
| Unallocated Billing Revenue | Approximately RWF 8.54 billion |

The gross billed revenue and payments collected measures were checked against their respective source tables.

The billing-to-appointment matching investigation revealed that only 5,000 of 60,000 billing records matched appointment records. Consequently, department-allocated revenue represents the matched portion rather than the full gross billed revenue.

The dashboard's RWF 0 Billing Revenue Reconciliation output was recorded for further investigation and was not treated as proof of complete reconciliation.

### Patient Demographics

| KPI | Result |
|---|---:|
| Total Patient Profiles | 20,000 |
| Male Patients | 10,090 (50.45%) |
| Female Patients | 9,910 (49.55%) |
| Average Patient Age | Approximately 45 years |

### Appointment Visit Types

The `VisitType` field was validated across all 5,000 appointment records.

| Visit Type | Count | Percentage |
|---|---:|---:|
| Emergency | 1,650 | 33.00% |
| Follow-up | 1,694 | 33.88% |
| Consultation | 1,656 | 33.12% |
| **Total** | **5,000** | **100%** |

Follow-up appointments represented the largest category, accounting for 33.88% of all appointment records.

These categories describe the type of visit and do not indicate whether an appointment was attended or missed.

### Diagnosis and Chronic Conditions

The diagnosis dataset contained approximately 60,000 diagnosis records.

| Diagnosis | Records |
|---|---:|
| Gastritis | 12,208 |
| Diabetes | 12,083 |
| Hypertension | 12,075 |
| Malaria | 11,878 |
| Upper Respiratory Infection | 11,756 |

Chronic condition records included:

- Asthma: 4,996
- Hypertension: 4,988
- Diabetes: 4,945

Zero orphaned diagnosis categories were identified. Diagnosis counts represent recorded diagnosis entries and should not be interpreted as unique patient counts or disease prevalence.

### Insurance Performance

The insurance claim approval rate was validated at **49.98%**.

Pending and blank claim statuses were not automatically classified as rejected claims.

## 2. Data Quality and Relationship Validation

The Week 7 review identified the following relationship results:

| Validation Area | Result |
|---|---:|
| Total Billing Records | 60,000 |
| Matched Billing Records | 5,000 |
| Unmatched Billing Records | 55,000 |
| Distinct Unmatched AppointmentIDs | 1,000 |
| Matched DepartmentIDs | 200 |
| Unmatched DepartmentIDs | 0 |
| Blank Appointment DepartmentIDs | 0 |

All 200 department identifiers in the appointment records matched the department reference data.

The main data integration concern was the large number of unmatched billing records.

## 3. Dashboard Functionality Testing

The interactive Power BI dashboard was tested to verify that users could navigate and interact with the analytical pages.

| Test | Result |
|---|---|
| Date slicer functionality | Pass |
| Department slicer functionality | Pass |
| Gender slicer functionality | Pass |
| KPI card responsiveness | Pass |
| Chart cross-filtering | Pass |
| Dashboard page navigation | Pass |
| Reset and clear filters | Pass |

The tested interactions worked as expected during the Week 7 review.

## 4. Analytical Findings

The validation process confirmed several important findings:

1. Gross billed revenue and collected payments matched their respective source totals.
2. Appointment visit types accounted for all 5,000 appointment records.
3. Patient gender distribution was relatively balanced.
4. Follow-up appointments represented the largest appointment category.
5. Department identifiers were fully matched across the reviewed appointment and department tables.
6. Billing-to-appointment matching remained a significant financial analysis limitation.
7. Facility mapping remained limited at approximately 5%.

## 5. Cross-Track Testing Contribution

The Data Science track reported testing its appointment-related emergency prediction model using:

- A locked hold-out test set.
- Label-shuffle testing.
- Time-based validation.
- Calibration checks.
- Segment-level checks.

Reported results included approximately 0.50 AUC on unseen data, compared with approximately 0.75 training AUC and 0.51 validation AUC.

The Data Science findings identified target-label inconsistencies and limitations in the underlying data. The model did not meet its release criteria, and the recommendation was not to deploy it until the data and target definition were improved.

These findings are documented as cross-track testing information relevant to the wider HealthConnect solution. The model testing results are attributed to the Data Science track.

## 6. Data Limitations

The Week 7 review identified the following limitations:

- **Billing integration:** 55,000 billing records remained unmatched to appointment records.
- **Revenue reconciliation:** Different revenue outputs require further reconciliation and investigation.
- **Facility mapping:** Approximately 5% mapping limits reliable facility-level analysis.
- **Attendance data:** The appointment dataset does not contain an attendance status field. Attendance and no-show rates cannot be calculated.
- **Bed utilization:** Available bed records do not provide reliable occupancy history.
- **Room utilization:** Reliable room occupancy information is unavailable.
- **Equipment utilization:** Equipment usage, downtime, and maintenance history are insufficient for actual utilization calculations.
- **Diagnosis interpretation:** Diagnosis counts represent records, not necessarily unique patients or disease prevalence.
- **Insurance status:** Pending and blank claim statuses require careful interpretation.

## 7. Recommendations

1. Investigate unmatched billing and appointment identifiers.
2. Improve financial reconciliation and clarify revenue measure definitions.
3. Improve facility master data and mapping.
4. Introduce appointment attendance status capture.
5. Integrate bed and room occupancy history.
6. Capture equipment usage and maintenance information.
7. Improve insurance claim status completeness.
8. Resolve Data Science target-label and source-data issues before model deployment.
9. Retest affected measures after data integration improvements.

## 8. Week 7 Deliverables

The Week 7 documentation includes:

- Testing plan.
- KPI validation record.
- Data quality validation record.
- Dashboard functionality testing.
- Analytical findings validation.
- Data Science cross-track collaboration record.
- Refinement and data limitations record.
- Screenshots and evidence index.

## Conclusion

Week 7 strengthened the HealthConnect Rwanda analytics solution through KPI verification, data relationship testing, dashboard functionality checks, and analytical validation.

The review confirmed several important dashboard outputs while identifying financial integration, facility mapping, attendance data, and resource utilization limitations.

The documented findings provide a basis for further integration, refinement, and final project preparation during Week 8.

**Project Status:** Week 7 testing and validation documentation completed. Remaining data integration issues are documented for follow-up.
