# Maternal Health Risk Screening — Group 6

Retrospective analysis of maternal-health risk classification,
probability reliability, error severity, and screening under
measurement and review-capacity constraints.

## Start here

- Final analysis notebook:
  [output/report_final_checks.ipynb](output/report_final_checks.ipynb)
- Final figures:
  [output/report_final_checks/figures](output/report_final_checks/figures)
- Final tables:
  [output/report_final_checks/tables](output/report_final_checks/tables)
- Recorded execution environment and input hashes:
  [run_manifest.json](output/report_final_checks/run_manifest.json)

The final-check notebook evaluates saved models and temperature
parameters; it does not refit the primary models.

## Analysis notebooks

| Notebook | Purpose |
|---|---|
| `01_cleaning_and_splitting.ipynb` | Data cleaning and partition preparation |
| `output/4.1_benchmark_verification.ipynb` | Model benchmarking and verification |
| `output/4.2_reliability_explainability.ipynb` | Probability reliability and explanations |
| `output/4.3_severity_analysis.ipynb` | Severity-aware decision policies |
| `output/4.4_adaptive_screening.ipynb` | Adaptive measurement acquisition |
| `4.5_capacity_prioritisation.ipynb` | Capacity-constrained ranking |
| `5_integrated_framework.ipynb` | Joint measurement and review constraints |
| `output/report_final_checks.ipynb` | Final report checks and visualisations |

Notebook numbering reflects development filenames and does not
exactly match the final report subsection numbering.

## Data and saved artifacts

`Mathernal_Risk.csv` is the input dataset.
The analysis retains 6,058 of 6,103 records after cleaning.

- `output/splits/`: fixed training, calibration, policy-validation,
  and test partitions.
- `output/train_cv_folds.csv`: stored training cross-validation folds.
- `output/models/`: saved models and model metadata.
- `output/section_4_2/`: saved temperature parameters and
  probability-analysis outputs.
- Other section folders contain intermediate analysis outputs.
- `output/report_final_checks/` contains the final report artifacts.

Preserve these paths: notebooks may depend on intermediate artifacts.

## Reproduction notes

The recorded final-check environment used Python 3.13.5.
Package versions and input SHA-256 hashes are in `run_manifest.json`.

The final-check notebook currently contains a machine-specific
BASE path. Update it to your local `output` directory before running.

Re-running data preparation or model development may overwrite
saved artifacts. Inspect notebook inputs and outputs before execution.
End-to-end execution on a clean environment has not yet been verified.

## Interpretation

Results concern dataset-defined risk labels and retrospective
allocation experiments. They do not establish clinical effectiveness,
causal effects, or readiness for autonomous clinical use.

SHAP explanations target calibrated High-risk probability.
Attributions describe model behaviour relative to the selected
background; they are not causal clinical effects.

## Contributions

| Member | Main report responsibilities |
|---|---|
| Trang | Sections 4.1–4.2 |
| Khanh | Methodology and Section 4.3 |
| Giang | Literature Review and Sections 4.4–4.5 |
| Châu | Section 4.6 and Section 5 |
| All members | Remaining sections, integration, review, and final checks |
