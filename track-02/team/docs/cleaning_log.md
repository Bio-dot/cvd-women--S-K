# Cleaning Log

Written by `01_cleaning.ipynb`. Rerun the notebook to update it.

| Dataset | Rule | Reason | Records before | Records after | Records affected |
|---|---|---|---|---|---|
| D1 | Drop duplicate ids | Each patient should appear once | 70,000 | 70,000 | 0 |
| D1 | Keep women only | Track focus on women | 70,000 | 45,530 | 24,470 |
| D1 | Keep ap_hi between 70 and 250 |  We are excluding improbable systolic readings while keeping a broader measurement range. | 45,530 | 45,379 | 151 |
| D1 | Keep ap_lo between 40 and 150 | We are exluding improbable diastolic readings while keeping a broader measurement range. | 45,379 | 44,775 | 604 |
| D1 | Keep rows where systolic > diastolic | Systolic is always higher than diastolic | 44,775 | 44,727 | 48 |
| D2 | Drop duplicate patient ids | Each record should appear once | 8,763 | 8,763 | 0 |
| D2 | Drop rows where blood pressure is not in 'number/number' form | Cannot be split | 8,763 | 8,763 | 0 |
