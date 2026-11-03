# HealthConnect Rwanda – Week 7 Data Limitations and Refinement Record

## 1. Purpose

This document records data limitations and analytical weaknesses identified while testing and validating the HealthConnect Rwanda Power BI dashboard.

The purpose is to distinguish confirmed findings from areas where the available data does not support reliable calculations or conclusions.

## 2. Billing-to-Appointment Matching Limitation

### Finding

The `HC_Billing` table contains 60,000 records, while `Fact_Appointments` contains 5,000 appointment records.

The matching review identified:

- 5,000 matched billing records.
- 55,000 unmatched billing records.
- 1,000 distinct unmatched AppointmentIDs.
- No blank billing AppointmentIDs reported.

The unmatched AppointmentIDs extend beyond the appointment records available in `Fact_Appointments`.

### Impact

Most billing records cannot be allocated to the corresponding appointment records through the current AppointmentID relationship.

This affects department-level revenue allocation and limits the completeness of financial analysis by department.

### Action / Recommendation

- Investigate the unmatched AppointmentIDs.
- Confirm whether the missing appointment records exist in another source.
- Review the integration and identifier-mapping process.
- Reconcile billing and appointment records before using the full billing dataset for department-level analysis.

## 3. Revenue Reconciliation and Summary Limitation

### Finding

The financial review recorded:

- Gross Billed Revenue: RWF 9.31 billion.
- Payments Collected: RWF 8.39 billion.
- Department Allocated Revenue: approximately RWF 771.13 million.
- Revenue Summary: RWF 1.13 billion.
- Unallocated Billing Revenue: approximately RWF 8.54 billion.
- Outstanding Balance: approximately RWF 920 million.
- Status-Based Outstanding: RWF 919.95 million.

The dashboard also displays RWF 0 for Billing Revenue Reconciliation.

### Impact

The different revenue outputs do not represent the same scope of records. In particular, Department Allocated Revenue is based on matched appointment records, while gross billed revenue covers the billing source data.

The zero reconciliation output should not be treated as proof that the financial datasets are fully reconciled.

### Action / Recommendation

- Investigate the Revenue Summary calculation and its source.
- Review the billing and payment relationships.
- Confirm the intended scope of each financial measure.
- Add reconciliation checks that clearly distinguish gross billed, collected, outstanding, allocated, and unallocated revenue.

## 4. Appointment Attendance and No-Show Data Limitation

### Finding

The `Fact_Appointments` dataset contains a `VisitType` field with three categories:

| Visit Type | Count |
|---|---:|
| Emergency | 1,650 |
| Follow-up | 1,694 |
| Consultation | 1,656 |
| **Total** | **5,000** |

However, the appointment dataset does not contain an attendance status field.

### Impact

The available data identifies the type of appointment but does not establish whether an appointment was:

- Attended.
- Missed / No-Show.
- Cancelled.

Consequently, attendance rates and no-show rates cannot be calculated reliably from the current appointment data.

### Action / Recommendation

Introduce an appointment attendance status field in the future integrated system, with clearly defined values such as:

- Attended.
- No-Show.
- Cancelled.

Once reliable attendance data becomes available, attendance and no-show indicators can be added to the dashboard.

**Validation decision:** Attendance Rate and No-Show Rate are recorded as Not Available – Data Limitation, not as failed or incomplete KPI calculations.

## 5. Facility Mapping Limitation

### Finding

Facility mapping is approximately 5%.

### Impact

The limited mapping restricts the reliability and completeness of facility-level comparisons.

### Action / Recommendation

- Review facility identifiers across the available datasets.
- Establish a consistent facility master reference.
- Resolve missing or inconsistent facility relationships.
- Revalidate facility-level dashboard outputs after mapping improvements.

## 6. Bed, Room and Equipment Utilization Limitation

### Bed Data

The available bed records indicate that all 2,000 beds are marked as Available.

There is no reliable occupancy history to establish how beds were used over time.

### Room Data

The available room information does not provide sufficient reliable occupancy information to calculate actual room utilization.

### Equipment Data

The equipment dataset contains 4,000 records, but does not provide sufficient operational usage, downtime, or maintenance history to establish actual equipment utilization.

### Impact

Availability alone does not demonstrate utilization. Calculating utilization from these fields would risk presenting misleading results.

### Action / Recommendation

Capture and integrate:

- Bed occupancy and discharge history.
- Room occupancy periods.
- Equipment usage records.
- Equipment downtime and maintenance history.

Until these data are available, bed, room, and equipment utilization rates should not be presented as validated performance indicators.

## 7. Diagnosis Interpretation Limitation

### Finding

The diagnosis dataset contains approximately 60,000 diagnosis records, and zero orphaned diagnosis categories were identified.

### Impact

The diagnosis counts represent recorded diagnosis entries. They do not automatically represent unique patients, disease prevalence, or confirmed population-level incidence.

### Action / Recommendation

Clearly label diagnosis visuals as diagnosis records or diagnosis counts. Use unique-patient calculations only where the necessary patient identifiers and relationships support them.

## 8. Insurance Claim Status Limitation

### Finding

The insurance approval rate was validated at 49.98%. The source data includes Pending and blank claim statuses.

### Impact

Pending and blank records cannot automatically be treated as rejected claims. Doing so could misrepresent the actual claim outcome distribution.

### Action / Recommendation

Maintain separate categories for approved, pending, rejected, and unknown or blank statuses where the source data supports them. Improve completeness of claim status capture.

## 9. Week 7 Refinement and Testing Summary

The following outcomes were recorded during the Week 7 review:

| Area | Finding / Outcome |
|---|---|
| Financial KPI validation | Gross billed revenue and payments collected matched their source totals. |
| Appointment visit types | All 5,000 records were accounted for across the three visit types. |
| Department mapping | All 200 department identifiers matched; no unmatched or blank department identifiers were reported. |
| Billing matching | 55,000 billing records remained unmatched to appointment records. |
| Dashboard interactions | Date, department and gender slicers, KPI responsiveness, chart cross-filtering, page navigation and reset/clear filters passed testing. |
| Attendance and no-show | Not calculable because attendance status is absent. |
| Facility analysis | Limited by approximately 5% facility mapping. |
| Resource utilization | Not validated because reliable usage and occupancy history is unavailable. |

No unconfirmed dashboard redesign or data correction is claimed in this record. The identified issues and recommended actions are documented for continued integration and refinement.

## 10. Recommendations for Week 8

1. Investigate and improve billing-to-appointment matching.
2. Review the Revenue Summary and financial reconciliation logic.
3. Improve facility master data and mapping.
4. Introduce reliable appointment attendance status capture.
5. Integrate bed, room and equipment usage history before calculating utilization.
6. Improve completeness and consistency of insurance claim statuses.
7. Preserve clear distinctions between diagnosis records and unique patients.
8. Retest affected KPIs and dashboard visuals after any changes.

---

**Document Status:** Week 7 data limitations and refinement record – updated with confirmed appointment visit types and validation findings.
