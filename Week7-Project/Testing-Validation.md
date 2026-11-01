### Overall Week 7 Testing Outcome

The HealthConnect Rwanda Data Analytics solution underwent analytical testing, KPI validation, dashboard functionality testing, data-model review and visual refinement.

The interactive dashboard was tested, and important financial and operational outputs were reviewed against the available datasets.

Testing revealed a significant appointment-to-billing integration gap: approximately 55,000 unmatched AppointmentIDs out of approximately 60,000 billing records. This resulted in RWF 771.13 million being allocated to matched appointments and approximately RWF 8.54 billion remaining unallocated.

Further validation identified a difference between the RWF 1.13 billion Revenue_Summary and RWF 9.31 billion HC_Billing total, as well as a RWF 50,000 difference between calculated and status-based outstanding balances.

The Star Schema review also highlighted blank department results, incomplete facility relationships, limitations in bed and equipment utilisation analysis, and inconsistencies between billing status and payment records.

Blank values were omitted from relevant analysis during data preparation. The identified limitations and unresolved integration issues were documented for Week 8.

**Final assessment:** Dashboard functionality has been tested and analytical refinement completed. The solution can proceed to Week 8 integration preparations, but full financial reconciliation, appointment matching and outstanding model issues must remain tracked before final project sign-off.
