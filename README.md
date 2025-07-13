🚲 Q3 2024 Bike-Share Analysis

Hi there—I’m Iheb, a data analyst. In this project I demonstrate a full ETL + descriptive-analytics workflow on Divvy bike-share trip data for Q3 2024, using DuckDB and JupyterLab.

---

🔍 Project Overview

- Objective:
  Clean, transform and summarize ride data to surface usage patterns (daily counts, ride durations, peak hours, etc.).
- Tech stack:
  - DuckDB for fast, local SQL querying
  - Pandas for DataFrame manipulation
  - Matplotlib for plotting
  - JupyterLab as the interactive notebook environment

---

🗂️ Repository Structure

q3-bike-analysis/
├── data/                         ← Your raw CSVs (not versioned)
│   └── 2024_Q3_csv/
│       ├── 202407_divvy_tripdata.csv
│       ├── 202408_divvy_tripdata.csv
│       └── 202409_divvy_tripdata.csv
├── Q3_2024_Data_Cleaned.ipynb    ← Parameterized Jupyter notebook
├── rides_2024_q3.db              ← DuckDB database (auto-generated)
├── .gitignore                    ← Ignores data/, .db, checkpoints
├── requirements.txt              ← Python dependencies
└── README.md                     ← (this file)

> Note: The `data/` folder and `.db` file are omitted from Git via `.gitignore`.

---

🚀 Quick Start

1. Clone this repo
   git clone https://github.com/Iheb-Tope/q3-bike-analysis.git
   cd q3-bike-analysis

2. Set up your environment
   conda create -n bike-env python=3.10 -y
   conda activate bike-env
   pip install --upgrade pip
   pip install -r requirements.txt

3. Add your data
   Place the three monthly CSVs into data/2024_Q3_csv/.

4. Run the notebook
   jupyter lab
   Open Q3_2024_Data_Cleaned.ipynb, update the YEAR & QUARTER at the top if needed, then Run ▶ All Cells.

---

📊 Key Analyses

- Daily Ride Counts: see how ridership waxes and wanes
- Hourly Distribution: identify peak commute times
- Ride Durations: compare mean & max by month
- Day-of-Week Mode: find the busiest weekday (with labels)

Charts and markdown commentary accompany each metric.

---

🔄 Extending to Other Quarters

1. Drop your new quarter’s CSVs into data/{YEAR}_Q{N}_csv/.
2. In the notebook’s first cell, set:
   YEAR    = 2024
   QUARTER = 2   # for Q2 (Apr–Jun), etc.
3. Run ▶ All Cells to regenerate the analysis.

---

📦 Dependencies

All Python packages are listed in requirements.txt. To install them:

pip install --upgrade pip
pip install -r requirements.txt

---

Feel free to fork, explore, or leave feedback!
