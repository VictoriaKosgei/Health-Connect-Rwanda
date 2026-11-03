# HealthConnect Rwanda – Data Science Cross-Track Collaboration Record

## 1. Purpose

This document records the Data Science cross-track testing findings relevant to the HealthConnect Rwanda analytics solution.

The collaboration focuses on evaluating the reliability of a predictive model intended to identify appointments that could lead to serious emergency cases.

## 2. Track Collaboration

- **Project:** HealthConnect Rwanda
- **Collaborating Track:** Data Science
- **Related Component:** Emergency-risk prediction model
- **Dependency:** Reliable appointment, attendance and admissions data.

## 3. Testing Activities Reported

The Data Science testing process included:

1. Locked hold-out testing.
2. Label-shuffle testing.
3. Time-based data splitting.
4. Model calibration checks.
5. Segment-level performance checks.
6. Comparison of training and validation performance.
7. Release-gate evaluation.

## 4. Findings

The reported unseen-data AUC was approximately 0.50, indicating performance close to random classification.

The model also showed a substantial difference between training and validation performance:

| Metric | Result |
|---|---:|
| Training AUC | 0.75 |
| Validation AUC | 0.51 |
| Unseen-data AUC | Approximately 0.50 |

Two known-answer checks reportedly demonstrated that the testing process could detect a real signal.

The investigation identified an unreliable target created by combining two unrelated labels.

## 5. Actions Reported

The Data Science testing process resulted in the following reported actions:

- Removal of unreliable fields.
- Simplification of the model.
- Replacement of an unsuitable threshold that flagged approximately 95% of patients.
- Addition of a release gate to define when the model should not be used.

## 6. Release Decision

The model did not meet the release requirements.

The recommendation was not to deploy the model until the underlying data and target definition were corrected.

Missing admissions and attendance records, together with broken table relationships, were identified as issues requiring attention.

## 7. Data Analytics Implications

The findings highlight the importance of:

- Reliable appointment records.
- Complete attendance information.
- Accurate admissions data.
- Consistent relationships between healthcare datasets.
- Clear and meaningful prediction targets.

These issues are relevant to the reliability of the wider HealthConnect Rwanda analytical solution.

## 8. Collaboration Contribution

The precise individual contribution of the Data Analytics intern and the information exchanged between tracks must be confirmed before this record is finalized.

## 9. Conclusion

The reported Data Science findings indicate that the emergency-risk model was not ready for deployment.

The model's limitations reinforce the need for stronger source-data quality, reliable target definitions and validated relationships before predictive outputs are used for healthcare decisions.
