"# PowerSINDy_Identifying_Nonlinear_Time_Dependent_Dynamics_in_Power_Grid_Frequency" 
# SINDy Grid-Frequency Analysis (SK vs CE)

This repository contains code and selected analysis artifacts for comparing SINDy-based models and optimizers on power-grid frequency dynamics.

## What this repository is for

The goal is to analyze and compare model behavior across:

- Datasets: South Korea (SK) and CE
- Model variants: `n2`, `n3`, `n2f1`
- Optimizers: `SR3`, `STLSQ`, `Lasso`

The workflow focuses on summary statistics, stability comparison, RMSE comparison, and visualization.

## Included in this upload

This repository currently includes:

- Analysis notebook:
  - `results-analysis_optimized.ipynb`
- Source scripts and utilities (example):
  - `compare_parameters.py`
  - `create-synthetic.py`
  - `my_functions.py`
  - `utils/`
- Environment specification:
  - `requirements.txt`
- Selected exported results/figures (examples):
  - `heatmap_lasso_alpha.pdf`
  - `omega_coefficient_summary.csv`
  - other CSV/PDF summary outputs used by notebooks

## Not included (intentionally)

Large raw/intermediate experiment result directories are not fully uploaded (for repository size and portability), such as:

- `result_sr3_ce/`
- `result_sr3_sk/`
- `results-ce-n2/`, `results-ce-n2f1/`, `results-ce-n3/`
- `results-sk-n2/`, `results-sk-n2f1/`, `results-sk-n3/`
- `sindy_results_parameters_*/`

As a result, some notebook cells that load local `.pkl` result files may show missing-file messages unless those directories are restored locally.

## Quick start

1. Create and activate a Python environment.
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open and run:

- `results-analysis_optimized.ipynb`

If needed, adjust path variables (for example `parent_dir`) inside the notebook to match your local folder layout.

## Reproducibility note

The current upload is designed for sharing analysis logic and selected outputs.

To fully reproduce every figure/table from raw chunk-level data, restore the omitted result directories listed above.

## Suggested repository structure hygiene

For GitHub use, keep source + curated outputs, and avoid committing large generated artifacts repeatedly.
A `.gitignore` is recommended to exclude virtual environments and bulky result folders.
