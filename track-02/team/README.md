# Team R&S: Cholesterol and CVD Labels in Women-Coded Records

OpenBio 2026 Datathon, Track 2: Cardiovascular Health in Women

> This project is a student data analysis. It is not medical advice, a diagnostic tool or clinical guidance.

## Team

| Name | Role |
|---|---|
|Sophia Snyder|All|

## Research Question

Among records coded as women in Dataset 1, how are age, blood pressure, cholesterol, and glucose associated with the recorded CVD label?

## Datasets Used

- [ ] Dataset 1: Cardiovascular Disease Dataset
- [ ] Dataset 2: Heart Attack Risk Prediction Dataset (synthetic)
- [ ] Dataset 3: Global CVD in Women, Tables S1 and S2
  
Dataset 1: Cardiovascular Disease Dataset*: individual-level records. We used records with gender code 1, identified as the shorter-height group from this file. Datasets 2 and 3 were not used in this analysis.
  
## How to Run

1. The raw files are already in `track-02/data/` (see the [data guide](../data/README.md)). On Colab the first notebook cell downloads them.
2. Install packages: `pip install -r requirements.txt`
3. Run `notebooks/01_cleaning.ipynb`, then `notebooks/02_analysis.ipynb`, top to bottom.

## Files

| Path | Contents |
|---|---|
| `notebooks/01_cleaning.ipynb` | Loads and cleans the data, writes the cleaning log |
| `notebooks/02_analysis.ipynb` | Summary statistics, models, checks and the headline visual |
| `src/` | Helper functions (optional) |
| `figures/` | Exported graphs, including `headline.png` |
| `docs/cleaning_log.md` | Each cleaning rule and the records affected |
| `docs/article.md` | Science communication article, following the [HUDP article guide](../../docs/article-guide.md) |
| `requirements.txt` | Python packages |

## Key Findings

[Two or three sentences with effect sizes and confidence intervals.]

## Limitations

- The measurements and CVD label were recorded at a medical exam. This analysis describes associations with the recorded label; it does not establish what caused disease or predict future disease.
- The outcome is common in this selected dataset, so odds ratios should not be described as risk ratios.
- The data record sex using a binary variable. We refer to the analyzed subset as “records coded as women” and do not generalize beyond the categories and records available.
- The systolic and diastolic blood-pressure limits were team-selected data-quality screening rules, not medical or diagnostic cutoffs.
- The AUC comes from one random split of this dataset. It does not establish performance in other populations or as a clinical tool.
- Cholesterol and glucose are coded categories, not continuous measurements.

## Presentation

Video link: [add your unlisted YouTube link]
