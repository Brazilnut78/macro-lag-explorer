# Macro Lag Explorer — Exploratory with Data

Python ETL → Power BI. Pulls FRED/Yahoo Finance data, aligns monthly (bronze/silver/gold), computes **CPI YoY** & **ΔFFR**, tags **hiking cycles**, and measures **months-to-cooling** using a 6-month trend within a 36-month window. QC charts in **Matplotlib**; visuals in **Power BI**.

## 🔗 Live Report (Public)
[View the report](https://app.powerbi.com/view?r=eyJrIjoiNjdiODJhNGUtOGYzYi00ODQwLTk2MmItZjNmNGI3ZDA0ZGNhIiwidCI6ImEyYjI4MjMwLWM5NjQtNDA3OC1hY2ExLTZiZGM3YTg4MjdjMiIsImMiOjJ9)

## ✨ Features
- ETL in Python (`pandas`, `requests`, `yfinance`)
- Layered outputs: **bronze / silver / gold** (CSV/Parquet)
- Metrics: CPI YoY, ΔFFR, Δ(CPI YoY) trend, months-to-cooling
- Extras: recession shading, lead–lag vs. S&P 500, event study

## 📊 Data Sources
- FRED: Headline CPI `CPIAUCSL`, Fed Funds `FEDFUNDS`, Recession `USREC`
- Yahoo Finance: S&P 500 `^GSPC`

## 🚀 Quickstart (Python 3.9+ recommended)
```bash
# 1) Create and activate a virtual environment
# Windows (PowerShell)
python -m venv .venv
.\.venv\Scripts\Activate

# macOS / Linux
# python3 -m venv .venv
# source .venv/bin/activate

# 2) Install dependencies
pip install -U pandas numpy matplotlib yfinance requests pyarrow notebook

# 3) Set your FRED API key
# Windows (PowerShell) — current session only:
$env:FRED_API_KEY="your_key_here"

# Windows (PowerShell) — persist for future sessions:
[System.Environment]::SetEnvironmentVariable("FRED_API_KEY","your_key_here","User")

# macOS / Linux — current session:
# export FRED_API_KEY="your_key_here"

# 4) Launch Jupyter and open the notebook
jupyter notebook Policy_Macro_Econ_Project.ipynb

```

## 📝 License 
MIT © Daniela Haskins — see [LICENSE](LICENSE).



