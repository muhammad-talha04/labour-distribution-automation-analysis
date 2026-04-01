# 🤖 Labour Distribution & Automation Risk Analysis — USA (2019–2024)

A data science project analysing how automation risk correlates with employment 
trends and wages across 600+ US occupations, using real BLS (Bureau of Labor 
Statistics) data from 2019 to 2024.

---

## 📌 Key Findings

- **Statistically significant negative relationship** between automation risk 
  and employment growth (slope: -0.1841, R²: 0.089, p < 0.0001)
- **High-risk occupations pay ~40% less** than low-risk ones ($51k vs $86k avg)
- **296 million workers** are in occupations with more than 70% automation risk
- Top at-risk jobs: Retail Salespersons, Cashiers, Office Clerks, Truck Drivers

---

## 📊 Charts Generated

| Chart | Description |
|-------|-------------|
| `disruption_vs_employment_change.png` | Scatter: automation risk vs employment change |
| `disruption_trend.png` | With OLS trend line |
| `disruption_validated.png` | With 95% confidence interval |
| `covid_sensitivity.png` | Full period vs Post-COVID comparison |
| `wage_vs_automation_risk.png` | Bubble chart: risk vs wages |
| `wage_vs_risk_clean.png` | Bar chart: wage and workers by risk tier |

---

## 🗂️ Project Structure
```
Labour_Distribution_Project/
├── data/
│   └── raw/        ← place downloaded BLS + automation files here
│
│── notebooks/
│   └── labour_distribution_project_code.ipynb
│
├── charts/
│   ├── disruption_trend.png
│   ├── disruption_validated.png
│   ├── covid_sensitivity.png
│   ├── wage_vs_automation_risk.png
│   └── wage_vs_risk_clean.png
│
├── output/
│   ├── labor_disruption_report.xlsx
│   └── weighted_risk_report.xlsx
│
└── README.md
```

---

## 📦 Data Sources

- **BLS Occupational Employment & Wage Statistics (OEWS):**
  https://www.bls.gov/oes/tables.htm
  Download: `oesm19all.zip` through `oesm24all.zip`

- **Automation Probability Data:**
  https://github.com/AAS27/Automation_of_occupations_consequences_for_the_USA
  Download and place in `data/raw/`

---

## 🛠️ Tech Stack

- **Python 3.10**
- `pandas` — data wrangling
- `numpy` — numerical operations
- `matplotlib` — visualizations
- `scipy` / `statsmodels` — statistical regression
- `openpyxl` — Excel report generation

---

## 🚀 How to Run

1. Clone this repository
2. Download the raw data files (links above) into `data/raw/`
3. Install dependencies:
```bash
   pip install pandas numpy matplotlib scipy statsmodels openpyxl
```
4. Open `notebooks/labour_distribution_project_code.ipynb` in Jupyter or VS Code
5. Run all cells

---

## 👤 Author

**Muhammad Talha**
[LinkedIn](https://www.linkedin.com/in/muhammad-talha04)
