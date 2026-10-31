# 🤖 Labour Distribution & Automation Risk Analysis — USA (2019–2024)

A data science project analysing how automation risk correlates with employment 
trends and wages across 600+ US occupations, using real BLS (Bureau of Labor 
Statistics) data from 2019 to 2024.

---

## 📌 Key Findings (BLS, May 2024)

- **High-risk occupations pay about 40% less.** Across 283 occupations with an
  automation probability of 70% or more, the average median wage is $51,423 a
  year. Across 198 low-risk occupations (under 30%), it is $86,048: a gap of
  $34,625.
- **55.6 million US workers** hold jobs in those high-risk occupations.
- Large high-risk occupations include Retail Salespersons, Cashiers, Office
  Clerks and Truck Drivers.

### Correction in progress

The first version of the employment-change analysis (2019 to 2024) summed the
industry breakdown rows in the BLS national file, so it counted the same
workers several times. I fixed the filter in the notebook (cross-industry rows
only, `naics == '000000'`) and cleared the affected outputs. I will publish the
employment-change slope and its charts again after re-running the notebook.
The wage results above come from the cross-industry rows and are unaffected.

### Limitations

- The automation probabilities come from Frey and Osborne (2013), not from a
  recent model of AI exposure.
- The comparison is correlational and works at the occupation level. It does
  not show that automation risk causes lower pay.
- Wage averages weight each occupation equally, not by headcount.

---

## 📊 Charts Generated

| Chart | Description |
|-------|-------------|
| `wage_vs_automation_risk.png` | Bubble chart: risk vs wages |
| `wage_vs_risk_clean.png` | Bar chart: wage and workers by risk tier |
| `disruption_vs_employment_change.png` | Risk vs employment change (stale, re-run pending) |
| `disruption_trend.png` | OLS trend line (stale, re-run pending) |
| `disruption_validated.png` | 95% confidence interval (stale, re-run pending) |
| `covid_sensitivity.png` | Full period vs post-COVID (stale, re-run pending) |

---

## 🗂️ Project Structure
```
Labour_Distribution_Project/
├── data/
│   └── raw/        
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

> ⚠️ Data files are not included in this repository due to size limits.
> Download them directly from the source links.

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
   pip install -r requirements.txt
```
4. Open `notebooks/labour_distribution_project_code.ipynb` in Jupyter or VS Code
5. Run all cells

---

## 👤 Author

**Muhammad Talha**
[LinkedIn](https://www.linkedin.com/in/muhammad-talha04)
