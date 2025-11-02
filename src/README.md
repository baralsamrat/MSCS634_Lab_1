# Lab: Data Collection, Visualization, and Statistical Analysis

**Student:** Samrat Baral  
**Course:** MSCS634 - Advanced Big Data and Data Mining  
**Instructor:** Satish Penmatsa  
**Dataset:** Flights (AirPassengers, 1949–1960)  
**Tool:** Google Colab (Python, Pandas, Matplotlib, scikit-learn)

---

## 🧠 Purpose
Demonstrate end-to-end data workflow: collection, visualization, preprocessing (missing values, outliers, reduction, scaling, discretization), and statistical analysis with clear evidence and rubric alignment.

---

## 📊 Key Steps & Evidence
- **Step 1: Data Collection & Loading**  
  - Dataset: `flights.csv` (AirPassengers, 1949–1960).  
  - Evidence: `/screenshots/step1_head.png`

- **Step 2: Visualizations**  
  - Line plot of average passengers per year → `/screenshots/step2_line_yearly.png`  
  - Bar chart of average passengers by month → `/screenshots/step2_bar_month.png`  
  - Insights → `/screenshots/step2_insights.png`

- **Step 3: Data Preprocessing**  
  - Missing values (introduced for demo), handled via forward/back fill:  
    - Before: `/screenshots/step3_missing_counts_before.png` + `/screenshots/step3_missing_before.png`  
    - After: `/screenshots/step3_missing_counts_after.png` + `/screenshots/step3_missing_after.png`  
  - Outliers (IQR):  
    - IQR calc: `/screenshots/step3_iqr_calc.png`  
    - Outliers: `/screenshots/step3_outliers.png`  
    - After handling: `/screenshots/step3_after_outlier.png`  
  - Reduction: sample 70% + drop `month` (keep `month_num`)  
    - Before: `/screenshots/step3_reduction_before.png`  
    - After: `/screenshots/step3_reduction_after.png`  
  - Scaling & Discretization (Min-Max; Low/Medium/High):  
    - Before: `/screenshots/step3_scaling_before.png`  
    - After: `/screenshots/step3_scaling_after.png`

- **Step 4: Statistical Analysis**  
  - `.info()` → `/screenshots/step4_info.png`  
  - `.describe()` → `/screenshots/step4_describe.png`  
  - Central tendency → `/screenshots/step4_central_tendency.png`  
  - Dispersion → `/screenshots/step4_dispersion.png`  
  - Correlation heatmap → `/screenshots/step4_correlation.png`

---

## 🔍 Key Insights
- Continuous growth in air travel from 1949–1960.  
- Seasonality peaks in July–August; troughs in early-year months.  
- Year is positively correlated with passenger counts.

---

## ⚙️ Challenges & Decisions
- The original dataset has no missing values; we introduced a few NaNs for demonstration to show techniques.  
- IQR rarely flags outliers here due to smooth seasonal trend; we still documented the method & result.  
- Chose Min-Max scaling to interpret results in [0,1] for easier discretization.

---

## 📁 Repository Structure
```
DataLab-Flights/
├── flights_lab.ipynb
├── flights.csv
├── evidence_before_missing.csv
├── evidence_after_missing.csv
├── evidence_after_outliers.csv
├── evidence_after_reduction.csv
├── evidence_after_scaling.csv
├── /screenshots/
│     ├── step1_head.png
│     ├── step2_line_yearly.png
│     ├── step2_bar_month.png
│     ├── step2_insights.png
│     ├── step3_missing_before.png
│     ├── step3_missing_counts_before.png
│     ├── step3_missing_counts_after.png
│     ├── step3_missing_after.png
│     ├── step3_iqr_calc.png
│     ├── step3_outliers.png
│     ├── step3_after_outlier.png
│     ├── step3_reduction_before.png
│     ├── step3_reduction_after.png
│     ├── step3_scaling_before.png
│     ├── step3_scaling_after.png
│     ├── step4_info.png
│     ├── step4_describe.png
│     ├── step4_central_tendency.png
│     ├── step4_dispersion.png
│     └── step4_correlation.png
└── README.md
```

---

## 🚀 How to Run
1. Open `flights_lab.ipynb` in Google Colab.  
2. Run cells top-to-bottom.  
3. Screenshots will be saved into `/screenshots` automatically when you run here or in Colab.

---

## 📦 Requirements
- pandas
- numpy
- matplotlib
- scikit-learn
