# Team_KDK_Code_V1

**SPE Africa Datathon 2026 — Team KDK's submission, analysing geothermal energy data from Utrecht, Netherlands.**

---

## Project Overview

This repository contains Team KDK's full data pipeline and analysis for the **SPE Africa Datathon 2026**, focused on the geothermal energy project in Utrecht, Netherlands. The work covers well log data preprocessing, missing data imputation, and predictive modelling using statistical and machine learning approaches.

---

## Team

**Team KDK**
- SPE Africa Datathon 2026

---

## Repository Structure

```
Team_KDK_Code_V1/
│
├── data/
│   ├── raw/               # Original, unmodified input data
│   └── processed/         # Cleaned and transformed data
│
├── notebooks/
│   └── well_log_preprocessing.ipynb   # Main analysis notebook
│
├── outputs/               # Plots, figures, and results
├── reports/               # Final report and presentation slides
├── src/                   # Reusable Python scripts
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

---

## Data

### Raw Data (`data/raw/`)

| File | Description |
|---|---|
| `BLT-01.las` | Well log — BLT-01 |
| `EVD-01.las` | Well log — EVD-01 |
| `JUT-01.las` | Well log — JUT-01 |
| `PKP-01.las` | Well log — PKP-01 |
| `target_lithologies.csv` | Main dataset (3,455 rows, 13 columns) |
| `Well Path Data.xlsx` | Well path/trajectory data for all 4 wells |

### Processed Data (`data/processed/`)

| File | Description |
|---|---|
| `BLT-01log.csv` | LAS converted to CSV |
| `EVD-01log.csv` | LAS converted to CSV |
| `JUT-01log.csv` | LAS converted to CSV |
| `PKP-01log.csv` | LAS converted to CSV |
| `target_lithologies_filled.csv` | Final cleaned dataset with imputed values |

---

## Methods

### Data Preprocessing
- Loaded well log data from LAS files and converted to CSV format
- Identified and filled missing values in three key columns:
  - **`depth_tvd_m`** — interpolated from well path trajectory data
  - **`bulk_density_gcc`** — predicted using a Random Forest Regressor (MAE: 0.0065 g/cc)
  - **`porosity_pct`** — computed via the Porosity-Density equation for EVD-01; predicted using Random Forest for JUT-01 (MAE: 0.3128%)

### Models Used
- **Random Forest Regressor** (`scikit-learn`) — for imputing missing bulk density and porosity values
- **Porosity-Density Equation** — physics-based formula using Slochteren Sandstone constants

$$\phi = \frac{\rho_{ma} - \rho_b}{\rho_{ma} - \rho_{fl}} \times 100$$

Where:
- $\rho_{ma}$ = 2.65 g/cc (quartz sandstone matrix density)
- $\rho_{fl}$ = 1.07 g/cc (saline formation brine density)

---

## Results

*Results and findings to be added.*

---

## Setup & Usage

### Requirements
- Python 3.11.2

### Installation

1. Clone or download the repository:
```bash
git clone https://github.com/sadaraka-kadi/Team_KDK_Code_V1.git
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Place the raw data files in `data/raw/`

4. Open and run the notebook:
```
notebooks/well_log_preprocessing.ipynb
```

> **Note:** Run cells in order. Processed files will be automatically saved to `data/processed/`.

---

## Dependencies

See [`requirements.txt`](requirements.txt) for the full list. Key libraries:

| Library | Purpose |
|---|---|
| `pandas` | Data manipulation |
| `numpy` | Numerical computing |
| `lasio` | Reading LAS well log files |
| `scikit-learn` | Machine learning (Random Forest) |
| `openpyxl` | Reading Excel well path data |

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
