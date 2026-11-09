# DSC8307 Data Mining, Modeling and Analytics — Advent 2026

This repository contains two reproducible projects, their executed Jupyter notebooks, datasets, and reports.

## Contents
- `Project_1_Bank_Marketing.ipynb` — term-deposit subscription classification.
- `Project_2_Concrete_Strength.ipynb` — concrete compressive-strength regression.
- `reports/Project_1_Report.docx` and `reports/Project_2_Report.docx` — project reports.
- `data/` — the two supplied CSV datasets.
- `requirements.txt` — Python dependencies.

## Run
Create and activate a Python environment, then run:
```bash
python -m pip install -r requirements.txt
jupyter notebook
```
Open each notebook and use **Kernel → Restart & Run All**. The notebooks load datasets from the relative `data/` directory.

## Methodological notes
Project 1 excludes `duration` from the operational models because it is unavailable before a call and would leak post-contact information. The validation set is used to select a threshold; the test set is reserved for final evaluation. The cost ratio used to illustrate threshold selection is an explicit business assumption, not a measured company cost.

Project 2 uses a fixed random train/test split and compares a linear model with nonlinear tree-based models. Results are predictive associations, not causal estimates.
