# HealthConnect Rwanda – Data Quality Validation

## 1. Purpose

This document records the data-quality checks performed during Week 7 to evaluate the consistency of identifiers and relationships across the HealthConnect Rwanda analytical model.

## 2. Appointment and Billing Validation

The relationship between `Fact_Appointments` and `HC_Billing` was investigated because unmatched appointment identifiers affected department-level revenue allocation.

### Validation Results

| Validation Check | Result |
|---|---:|
| Fact_Appointments Records | 5,000 |
| Matched Appointment IDs | 5,000 |
| HC_Billing Records | 60,000 |
| Unmatched Billing Records | 55,000 |
| Distinct Unmatched Appointment IDs | 1,000 |
| Blank Billing Appointment IDs | 0 |

### Finding

The 5,000 appointment identifiers in `Fact_Appointments` matched appointment identifiers in the billing data.

However, 55,000 billing records were associated with 1,000 distinct appointment identifiers that did not exist in the 5,000-record appointment table.

The additional appointment identifiers ranged from 5001 to 6000.

This mismatch affected the allocation of billing revenue to departments.

## 3. Department Identifier Validation

The department identifier relationship was also tested.

| Validation Check | Result |
|---|---:|
| Matched Department IDs | 200 |
| Unmatched Department IDs | 0 |
| Blank Department IDs | 0 |

### Finding

All 200 department identifiers used in the appointment records matched the department master data.

No unmatched or blank department identifiers were identified in this validation.

## 4. Financial Data Implication

The unmatched billing records created a difference between total gross billed revenue and revenue that could be allocated to departments through matched appointments.

The analysis therefore distinguishes:

- Total Gross Billed Revenue: RWF 9.31 billion.
- Department Allocated Revenue: approximately RWF 771.13 million.

The department-level analysis excludes the unmatched billing records rather than assigning them to incorrect departments.

## 5. Actions Taken

1. Investigated the appointment identifier mismatch.
2. Identified the unmatched billing records.
3. Confirmed the number of distinct unmatched appointment identifiers.
4. Checked department identifier consistency.
5. Used matched appointment records for department revenue allocation.
6. Documented the financial interpretation and limitation.

## 6. Conclusion

The department identifier relationship passed validation.

The appointment-to-billing relationship requires further investigation because a substantial number of billing records cannot be linked to the available appointment records.

The issue should be addressed through source-data reconciliation before complete department-level financial reporting is relied upon.
