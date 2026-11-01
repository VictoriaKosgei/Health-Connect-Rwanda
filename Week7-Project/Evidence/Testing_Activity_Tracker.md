# HealthConnect Rwanda – Testing Activity Tracker

## 1. Purpose

This tracker documents the analytical testing and validation activities performed during Week 7. It records the areas tested, observations, results, supporting evidence, and outstanding issues requiring attention before final project integration.

## 2. Testing Activity Register

| ID | Testing Activity | Expected Outcome | Observation / Result | Status | Evidence |
|---|---|---|---|---|---|
| TA01 | Total Appointments Validation | Appointment count should reflect the appointment dataset. | Dashboard displays 5,000 appointments. | Reviewed | EV01 |
| TA02 | Billing Appointment Count | Billing records should be counted accurately. | Dashboard displays approximately 60K billing appointment records. | Reviewed | EV05 |
| TA03 | AppointmentID Matching | Billing AppointmentIDs should be matched against appointment records. | Approximately 55K unique unmatched AppointmentIDs identified. | Pending | EV05 |
| TA04 | Department Revenue Allocation | Revenue should be allocated to matched appointment records where relationships permit. | Department Allocated Revenue recorded as RWF 771.13 million. | Reviewed | EV06 |
| TA05 | Unmatched Billing Revenue | Unmatched billing records should be identified separately from matched revenue. | Approximately RWF 8.54 billion remains associated with unmatched records. | Pending | EV07 |
| TA06 | Revenue Reconciliation | Revenue reconciliation should produce a zero difference when the compared values agree. | Dashboard displays a reconciliation difference of 0; underlying revenue discrepancies still require investigation. | Pending | EV08 |
| TA07 | Revenue Summary Comparison | Revenue_Summary should reconcile with HC_Billing totals. | Approximate RWF 1.13 billion versus RWF 9.31 billion identified as a discrepancy. | Pending | EV08 |
| TA08 | Star Schema Review | Relationships should support the intended dimension-to-fact filtering. | Model and relationship behaviour require further review. | Pending | EV09 |
| TA09 | Department Filtering | Department selections should return the expected allocated revenue. | Blank department results were observed. | Pending | EV10 |
| TA10 | Blank Value Handling | Blank values should be handled consistently during preparation and analysis. | Blank values were omitted during the relevant preparation and analysis activities. | Reviewed | EV04 |
| TA11 | Dashboard Filter Testing | Dashboard filters should respond to user selections. | Dashboard filter interactions were tested. | Tested | EV11 |
| TA12 | Dashboard Refinement | Dashboard visuals should be clear and support analytical interpretation. | Refinement activities documented for the Week 7 dashboard. | In Progress | EV12 |

## 3. Outstanding Issues

The following issues require further investigation or reconciliation:

1. **AppointmentID mismatch:** Approximately 55K unique unmatched AppointmentIDs require investigation.
2. **Unmatched billing revenue:** Approximately RWF 8.54 billion is associated with unmatched records and has not been allocated through the appointment matching process.
3. **Revenue discrepancy:** Revenue_Summary reports approximately RWF 1.13 billion compared with approximately RWF 9.31 billion in HC_Billing.
4. **Department filtering:** Blank department results require relationship and key validation.
5. **Revenue reconciliation:** A displayed zero difference does not, by itself, resolve the underlying revenue discrepancies.
6. **Final integration:** Cross-track integration and final KPI validation remain part of Week 8 readiness.

## 4. Testing Status Summary

| Status | Meaning |
|---|---|
| Reviewed | The relevant value or process has been examined. |
| Tested | The functionality has been tested. |
| In Progress | Work is ongoing. |
| Pending | Further investigation or validation is required. |
| Resolved | Issue has been corrected and supported by evidence. |

## 5. Week 8 Follow-Up Actions

- Investigate unmatched AppointmentIDs and confirm the appropriate matching approach.
- Review the relationships between appointment, billing, and department records.
- Investigate the Revenue_Summary and HC_Billing discrepancy.
- Confirm the meaning and calculation of the revenue reconciliation measure.
- Revalidate department-level revenue allocation.
- Complete cross-track integration checks.
- Perform final dashboard and KPI validation.
- Update the issue log and evidence register with verified outcomes.

## 6. Conclusion

Week 7 testing identified important data matching, revenue reconciliation, and relationship-filtering issues within the HealthConnect Rwanda analytical model. The findings have been documented to support transparent reporting and guide the remaining validation activities.

Outstanding issues will be carried forward for investigation and resolution during Week 8. No unresolved issue should be marked as passed or resolved without supporting validation evidence.
