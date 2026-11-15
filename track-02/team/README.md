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

- [Y] Dataset 1: Cardiovascular Disease Dataset
- [ ] Dataset 2: Heart Attack Risk Prediction Dataset (synthetic)
- [ ] Dataset 3: Global CVD in Women, Tables S1 and S2
- **Dataset 1: Cardiovascular Disease Dataset** — individual-level records. We used records with gender code 1, identified as the shorter-height group in this file.
- Datasets 2 and 3 were not used in this analysis.
  
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

[Synthetic data, ecological fallacy, binary sex variable, anything else that limits your claims.]

## Presentation

Video link: [add your unlisted YouTube link]
