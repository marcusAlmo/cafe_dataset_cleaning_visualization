# Cafe Sales Analysis Notebooks

This directory contains Jupyter notebooks for analyzing and visualizing cafe sales data. The analysis is split into two main notebooks: data health checking and visualization.

## Setup

Requirements:
- Python 3.x
- Jupyter Notebook/VS Code with Jupyter extension
- Required packages: 
  ```bash
  pip install pandas matplotlib seaborn
  ```

## Notebooks Overview

### 1. `data_health_check.ipynb`
Initial data quality assessment and cleaning notebook.

**Key Features:**
- Transaction ID validation
- Item categorization check
- Error entry identification
- Data cleaning operations
  - Converting 'ERROR' entries to 'Void'
  - Handling unknown values
  - Date format standardization

**Output:**
- Clean dataset saved as `../data/cleaned/clean_cafe_sales.csv`

### 2. `data_visualization.ipynb`
Comprehensive visualization of sales patterns and trends.

**Key Features:**
- Monthly transaction analysis
  - Combined visualization of transactions and revenue
  - Dual-axis plots showing correlation between sales volume and revenue
  - Peak transaction period identification

- Item-specific analysis
  - Individual item performance tracking
  - Per-product revenue analysis
  - Monthly trends for specific products (e.g., Coffee)

**Visualizations Include:**
1. Monthly Overview
   - Combined transactions/revenue plot
   - Individual transaction trend
   - Individual revenue trend

2. Product-Specific Analysis
   - Product-wise transaction counts
   - Product revenue analysis
   - Monthly trends per product

## Usage Guide

1. Start with `data_health_check.ipynb`
   - Run all cells in sequence
   - Verify data cleaning results
   - Check for any remaining data quality issues

2. Proceed to `data_visualization.ipynb`
   - Ensure clean data file is present
   - Run initialization cells
   - Execute visualization cells
   - For product-specific analysis:
     1. View available products list
     2. Update `item` variable with desired product
     3. Run subsequent cells for analysis

## Data Source
Dataset: [Cafe Sales (Dirty Data for Cleaning Training)](https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training)
Platform: Kaggle

## Notes
- Visualizations can be further enhanced using BI tools
- The notebooks are designed to be run sequentially
- Each visualization section includes separate plots for detailed analysis
- All plots include proper labeling and legends for clarity

Created by: Mark June Almojuela
Last Modified: 11-10-2025