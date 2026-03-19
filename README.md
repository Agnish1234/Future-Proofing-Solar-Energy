# Future‑Proofing Solar Energy: A Multi‑Model Assessment of Climate Change Impacts on Photovoltaic Site Suitability

---

## 📌 Overview

**If we build solar farms today based on today's weather, will they still be good investments 25 years from now when the climate has changed?**

This project answers that question. It provides a complete, reproducible data analysis pipeline that integrates **future climate projections (2050)** with a suite of statistical learning methods—hypothesis testing, ANOVA, linear/logistic regression, clustering, and decision trees—to identify locations where solar photovoltaic (PV) investments remain robust under climate change.

Unlike traditional site‑suitability studies that rely only on current climate data, this work explicitly accounts for **climate‑induced changes in irradiance and temperature**, helping energy planners, policymakers, and investors make long‑term, resilient decisions.

The analysis is demonstrated on a **realistic synthetic dataset** for a region in eastern India (22–24°N, 88–90°E), but the code is modular and ready to be applied to real data from sources like WorldClim, NASA POWER, or the Global Solar Atlas.

---

## 🎯 Key Findings (In Plain English)

- **Climate change will alter solar suitability.** The difference between today and 2050 is statistically significant (p < 0.001). Some sunny places today will become too cloudy or too hot.
- **Sunlight is king, but heat matters.** Irradiance explains ~90% of suitability, but temperature is a close second. The best spots have **high sun AND moderate temperatures**.
- **Land cover matters consistently.** Barren land is best; water and forest are worst. Policy incentives (near cities) help equally everywhere—they don’t change the ranking of land types.
- **Three distinct risk zones emerge.** A simple “traffic light” map shows where to invest (green), where to be cautious (yellow), and where to avoid (red).
- **Simple rules work.** The decision tree gives easy‑to‑remember thresholds (e.g., “if irradiance > 4.9 kWh/m²/day and temperature < 25°C, suitability is high”).
- **Models are accurate.** Linear regression R² = 0.84, logistic regression AUC = 0.95, decision tree R² = 0.73 (on test data).

---

## 📊 Results at a Glance

| Metric | Value |
|--------|-------|
| Suitability change (Wilcoxon test) | p < 0.001 (significant) |
| Linear regression R² | 0.836 |
| Logistic regression AUC | 0.952 |
| Optimal number of clusters | 3 (silhouette score 0.204) |
| Most important feature (decision tree) | Irradiance (90% importance) |
| Decision tree test R² | 0.730 |

### Example Visuals

| Current Suitability | Future Suitability (2050) | Clusters (Risk Zones) |
|---------------------|---------------------------|------------------------|
| ![](figures/suitability_maps.png) | ![](figures/suitability_maps.png) | ![](figures/cluster_map.png) |

*(Note: The maps above show the same figure as a placeholder; replace with your actual images after uploading to the `figures/` folder.)*

All 12 publication‑ready figures are available in the [`figures/`](./figures) directory.

---

## 🧠 Methodology

The analysis follows a structured workflow that mirrors the NPTEL Data Analytics syllabus:

1. **Data Generation** – Realistic synthetic environmental data with spatial autocorrelation.
2. **Suitability Index** – Weighted combination of irradiance, temperature, slope, grid distance, and land cover.
3. **Exploratory Data Analysis** – Histograms, correlation matrix, spatial maps.
4. **Hypothesis Testing** – Wilcoxon signed‑rank test for change in suitability.
5. **ANOVA** – One‑way and two‑way ANOVA to assess land cover and policy zone effects.
6. **Multiple Linear Regression** – Standardized predictors, VIF, residual diagnostics, spatial autocorrelation (Moran’s I).
7. **Logistic Regression & ROC** – Binary suitability classification, AUC = 0.95.
8. **Clustering** – k‑means with silhouette analysis to identify risk zones.
9. **Decision Tree** – Interpretable regression tree with simple rules.
10. **Reproducibility** – All code, data, and figures saved.

Each step is explained in simple language within the notebook.

---

## 📁 Repository Structure
