# Cafe Sales — Data Engineering Project

A small end-to-end data engineering and analysis project that cleans, analyzes, and visualizes a cafe sales dataset. The project demonstrates data quality checks, cleaning techniques, time-series aggregation, and visualizations using Python (Pandas, Matplotlib, Seaborn) in Jupyter/VS Code notebooks.

---

## Project Summary

This repository contains notebooks and data for exploring a noisy "dirty" cafe sales dataset from Kaggle. The work includes:

- Data quality assessment and validation (transaction IDs, missing values, malformed entries).
- Data cleaning and normalization (e.g., standardizing error/unknown items, date parsing).
- Time-series aggregation to compute monthly transactions and revenues.
- Visualizations comparing transaction volume and revenue (dual-axis plots) and item-level analyses.

Skills & techniques: data cleaning, exploratory data analysis (EDA), time-series aggregation, plotting and visualization, reproducible notebooks.


## Repository structure

- data/
  - raw/ — original imported CSVs (e.g., `dirty_cafe_sales.csv`)
  - cleaned/ — output cleaned dataset(s)
- notebooks/
  - `data_health_check.ipynb` — initial data checks and cleaning steps
  - `data_visualization.ipynb` — aggregations and visualization routines
  - `README.md` — (notebooks folder) quick notes about running the notebooks
- README.md — this file


## Data source

Kaggle: "Cafe Sales (Dirty Data for Cleaning Training)"
https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training


## Setup (Windows PowerShell)

1. Create and activate a virtual environment (optional but recommended):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install dependencies:

```powershell
pip install pandas matplotlib seaborn jupyter
```

(You can also open the notebooks directly in VS Code with the Python and Jupyter extensions.)


## How to run

1. Start by running the notebook `notebooks/data_health_check.ipynb` top-to-bottom. This notebook:
   - Loads the raw CSV from `data/raw/`.
   - Prints data info, checks Transaction IDs, surfaces invalid entries (e.g., 'ERROR', 'UNKNOWN').
   - Replaces bad item labels (e.g., `'ERROR' -> 'Void'`) and standardizes dates.
   - Produces or writes a cleaned CSV to `data/cleaned/clean_cafe_sales.csv` (if saving is included).

2. Open `notebooks/data_visualization.ipynb` after the cleaning step and run cells to:
   - Compute a `Month` period column from `Transaction Date`.
   - Aggregate monthly transactions and total revenue.
   - Plot combined monthly transactions (blue) and revenue (red) using a dual-axis plot.
   - Inspect and plot item-level trends by updating the `item` variable in the item-analysis cells.


## Key Notebook Highlights

- `data_health_check.ipynb`
  - Transaction ID validation (prefix checks, uniqueness)
  - Item value checks and replacements
  - Date parsing and validity checks
  - Unique-items count and frequency breakdown

- `data_visualization.ipynb`
  - Engineering a `Month` Period column and aggregating:
    - `monthly_transactions = valid_dates.groupby('Month').size()`
    - `monthly_revenues = valid_dates.groupby('Month')['Total Spent'].sum()`
  - Combined plot of transactions (left axis) and revenue (right axis)
  - Item-specific monthly trends and revenue plots


## Example commands (PowerShell)

Open Jupyter Notebook/Lab:

```powershell
jupyter notebook
# or
jupyter lab
```

Open the project in VS Code, then run notebooks with the interactive runner.


## Suggestions & Next Steps

- Add a `requirements.txt` or `environment.yml` for reproducibility.
- Persist cleaned datasets to `data/cleaned/` with a timestamped filename.
- Add unit checks/assertions to the cleaning notebook (e.g., assert no remaining `'ERROR'` values).
- Create PNG/SVG exports of key charts for README previews or portfolio presentation.


## About

Author: Mark June Almojuela
Last modified: 2025-11-10

If you'd like, I can:
- Add a `requirements.txt` file,
- Add example chart images to include in this README,
- Or generate a short project blurb optimized for GitHub profile/portfolio usage.

