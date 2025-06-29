# Q3 2024 Bike Rides ETL & Analysis Notebook

This repository contains a Jupyter Notebook that demonstrates an end-to-end ETL (Extract, Transform, Load) pipeline and exploratory analysis for Q3 2024 bike rides data. We use DuckDB for SQL-based ingestion, cleaning, and aggregation, and pandas/matplotlib for visualization.

## Repository Structure

q3-bike-analysis/
├── Q3_2024_Data_Cleaned.ipynb ← Your notebook
├── data/
│ └── 2024_Q3_csv/ ← July, August & September CSVs
├── requirements.txt ← Python dependencies
└── README.md ← This file

## Setup & Installation

1. **Open Anaconda Prompt** (or your terminal) and navigate to this folder:
   cd %USERPROFILE%\Downloads\q3-bike-analysis
   
2. **Create & activate the Conda environment (if you haven’t already)**:

conda create --name q3analysis python=3.9 -y
conda activate q3analysis

3. **Install dependencies**:
pip install --upgrade pip
pip install -r requirements.txt

## Running the Notebook
1. Launch Jupyter:
jupyter notebook
2. In the browser file listing, click Q3_2024_Data_Cleaned.ipynb.
3. Select Kernel → Restart & Run All to execute every cell in order.

## Note: Make sure the data/2024_Q3_csv/ folder contains your three CSVs (202407, 202408, 202409).

## Notebook Overview

1. Data Ingestion
Combines the three month CSVs into a DuckDB view.

2. Data Cleaning

Filters to rides starting in Q3 (July 1 – September 30).

Drops nulls, duplicates, and outliers (< 1 min or > 24 h).

Rounds lat/lng to 4 decimals.

Derives ride_length and day_of_week.

3. Exploratory Analysis

Summaries: daily counts & average duration; hourly patterns; member vs. casual; top stations.

Descriptive stats: mean, max, median, mode by month and for the quarter.

Visuals: time series and bar charts via matplotlib.

4. Export
Exports key summary tables to CSV for reporting or further exploration.

## Environment & Reproducibility

Python 3.9+

DuckDB (for zero-config SQL)

pandas, matplotlib, jupyter

See requirements.txt for exact versions. To recreate the environment:

conda env create -f environment.yml   # if you exported one
# or
pip install -r requirements.txt

## (Optional) Binder Launch 
Add this badge at the top of your README to let anyone run your notebook in the cloud:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/your-username/q3-bike-analysis/main)

## Next Steps & Extensions

Build an interactive dashboard with Streamlit or Voilà.

Perform geospatial station clustering.

Forecast Q4 demand with time-series models.

## This project demonstrates a professional, reproducible SQL + Python workflow
1. **Create** a file named `README.md` in `C:\Users\ihebb\Downloads\q3-bike-analysis\`.  
2. **Paste** the above Markdown into it and **save**.  
3. **Refresh** your Jupyter file browser—you’ll now see `README.md` alongside your notebook and data.
