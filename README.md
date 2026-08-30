# SALES-ANALYSIS

This repository contains an end-to-end exploratory data analysis (EDA) of a sales dataset. The analysis is implemented as a Google Colab / Jupyter notebook and demonstrates typical data cleaning, enrichment, analysis, and visualization steps to extract business insights from transactional sales data.

## Contents
- `SALES ANALYSIS.ipynb` — Main Colab/Jupyter notebook with the full analysis.
- `events.csv` — Transactional sales data (Order ID, Order Date, Ship Date, Country Code, Product ID, Sales Channel, Units Sold, Unit Price, Unit Cost, ...).
- `products.csv` — Product lookup table (product id & item type/category).
- `countries.csv` — Country lookup with ISO codes and region/sub-region information.

> Note: The CSV files are expected to be in the same folder as the notebook or accessible from Google Drive when running in Colab.

## Summary
The notebook performs the following steps:
- Load CSV files into pandas DataFrames.
- Parse and normalize date columns (`Order Date`, `Ship Date`).
- Inspect and clean missing values and duplicates.
- Merge `events` with `products` and `countries` to enrich transactions with product categories and geographic information.
- Compute derived metrics such as revenue, cost, and profit/margin.
- Perform exploratory analyses and visualizations, including:
  - Total sales and profit by region and country.
  - Sales by product category and top-selling products.
  - Comparison of Online vs Offline sales channels.
  - Time-series analysis to inspect seasonality and trends.

## Requirements
- Python 3.7+
- pandas
- numpy
- matplotlib
- seaborn

If running locally, install requirements with:

```bash
pip install pandas numpy matplotlib seaborn
```

## How to run
1. Open `SALES ANALYSIS.ipynb` in Google Colab or Jupyter Notebook.
2. If using Colab, mount Google Drive (the notebook includes code to mount Drive) and place the CSV files in the referenced directory, or update the file paths accordingly.
3. Run the notebook cells sequentially to reproduce the analysis and figures.

## Results and Next Steps
The notebook surfaces key findings (top markets, best-performing product categories, channel performance, and temporal trends) and contains plots to help communicate these insights. Suggested next steps:
- Build a dashboard (e.g., with Streamlit or Dash) to make the insights interactive.
- Add more granular analyses (cohort analysis, customer segmentation) if customer identifiers become available.
- Automate the pipeline to refresh insights when new data arrives.

## Contributing
Feel free to raise issues or submit pull requests to improve the notebook, add tests, or add reproducible scripts for production workflows.
