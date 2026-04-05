# 🌍 Global Compound Climate Risk Regimes (1990–2023)

### Detection, Predictability, and Attributable Drivers using ERA5 Surface Data

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Status](https://img.shields.io/badge/Status-Research-green)
![Data](https://img.shields.io/badge/Data-ERA5-orange)

---

## 📌 Overview

This project presents a **data-driven framework** to analyze **global compound climate risk regimes** using ERA5 monthly surface reanalysis data from **1990 to 2023**.

Unlike traditional approaches that focus on single variables or isolated extreme events, this study identifies **recurring multivariate climate patterns (regimes)** by integrating multiple atmospheric variables into a unified analytical pipeline.

---

## 🎯 Objectives

- Identify **dominant global climate risk regimes**
- Develop a **data-driven multivariate climate index (MCSI)**
- Evaluate **predictability of regime transitions**
- Explain **key drivers using explainable AI (SHAP)**
- Detect **long-term trends and emerging hotspots**

---

## ❗ Research Gaps Addressed

| Gap in Previous Studies | Our Approach |
|------------------------|-------------|
| Manually weighted indices | PCA-based data-driven index (MCSI) |
| Regional or limited scope | Global analysis (1990–2023) |
| Limited variables | Integration of 6 surface climate variables |
| Event-based analysis | Regime-based clustering approach |
| No prediction benchmarking | ML models evaluated against persistence baseline |
| Black-box ML | SHAP-based explainability |
| Weak trend reliability | Mann-Kendall + FDR correction |
| Fragmented methodologies | Fully integrated analytical pipeline |

---

## 📊 Dataset

- **Source:** ERA5 Reanalysis (Copernicus Climate Data Store)  
- **Link:** https://cds.climate.copernicus.eu/  
- **Temporal Coverage:** 1990–2023  
- **Resolution:** Monthly averages  

### Variables Used:
- 2m Temperature (`t2m`)
- Total Precipitation (`tp`)
- Precipitation Rate (`avg_tprate`)
- Surface Solar Radiation (`ssr`)
- Total Cloud Cover (`tcc`)
- 10m Wind Speed (`si10`)

---

## ⚙️ Methodology

### 🔹 1. Preprocessing
- Convert raw data into **monthly anomalies**
- Standardize variables to ensure comparability

---

### 🔹 2. Multivariate Climate State Index (MCSI)
- Apply **Principal Component Analysis (PCA)**
- Extract **first principal component (PC1)** as the climate state index

---

### 🔹 3. Regime Detection (Unsupervised Learning)
- Algorithms used:
  - K-Means
  - Gaussian Mixture Model (GMM)
  - HDBSCAN
- Output: **Distinct climate regimes (clusters)**

---

### 🔹 4. Predictability Analysis (Supervised Learning)
- Models:
  - Random Forest
  - XGBoost
- Task: Predict **next-month climate regime**

#### Baseline:
- Persistence assumption (next state = current state)

#### Skill Score:

