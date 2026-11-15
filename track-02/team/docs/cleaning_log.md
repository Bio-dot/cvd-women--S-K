# Cleaning Log

Written by `01_cleaning.ipynb`. Rerun the notebook to update it.

| Dataset | Rule | Reason | Records before | Records after | Records affected |
|---|---|---|---|---|---|
| D1 | Drop duplicate ids | Each patient should appear once | 70,000 | 70,000 | 0 |
| D1 | Keep women only | Track focus on women | 70,000 | 45,530 | 24,470 |
| D1 | Keep ap_hi between 70 and 250 |  We are excluding improbable systolic readings while keeping a broader measurement range. | 45,530 | 45,379 | 151 |
| D1 | Keep ap_lo between 40 and 150 | We are excluding improbable diastolic readings while keeping a broader measurement range. | 45,379 | 44,775 | 604 |
| D1 | Keep rows where systolic > diastolic | Systolic is always higher than diastolic | 44,775 | 44,727 | 48 |
| D2 | Drop duplicate patient ids | Each record should appear once | 8,763 | 8,763 | 0 |
| D2 | Drop rows where blood pressure is not in 'number/number' form | Cannot be split | 8,763 | 8,763 | 0 |

## Scope and additional decisions

The primary analysis uses Dataset 1 and records coded as women (gender code 1, checked by comparing mean height between gender codes). The 24,470 records not coded as women were excluded from this women-focused analysis. They were not treated as erroneous records.

The final cleaned Dataset 1 file, `data_clean/d1_clean.csv`, contains 44,727 records. Our team selected blood-pressure ranges (systolic 70–250 mmHg; diastolic 40–150 mmHg) are data quality screening rules for this analysis, not medical or diagnostic cutoffs.

Height and weight were inspected but not range-filtered because they are not predictors in this analysis. BMI was not calculated or used. Dataset 2 was not used for the primary analysis; its entries above reflect notebook checks that affected zero records and do not contribute to the reported findings.
