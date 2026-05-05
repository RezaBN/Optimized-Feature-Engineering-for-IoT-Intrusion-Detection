# Intrusion Detection Pipeline Benchmark Results

This repository contains the **experimental results** of our study on the impact of **feature selection (FS)** and **feature extraction (FE)** techniques in machine learning-based intrusion detection systems (IDS).

## 📊 Overview

The experiments are conducted on three widely used benchmark datasets:

* UNSW-NB15
* AWID
* CSE-CIC-IDS2018

The study evaluates a comprehensive pipeline:

> **Balancing → Scaling → Feature Selection → Feature Extraction → Classification**

The total **pipeline configurations per dataset** were explored, combining:

* **Feature Selection (FS):** Variance Threshold (VT), ANOVA F-test, Chi-Squared (Chi2)
* **Feature Extraction (FE):** PCA, LDA, ICA, SVD
* **Classifiers (12 models):**
  DT, LR, KNN, NB, SVM, RF, ET, GB, XGB, LGBM, CAT, STACK

## 📁 Repository Contents

The repository includes the following result files:

### 1. Cross-Validation Summary Results

* `cv_results_summary.csv`

  * Aggregated performance across all configurations
  * Metrics reported as **mean ± standard deviation**
  * Includes Macro-F1 and Weighted-F1 scores

### 2. Fold-Level Results

* `cv_fold_level_records.csv`

  * Detailed performance for each fold
  * Enables reproducibility and statistical analysis

### 3. Ablation Study Results

* `ablation_modellevel_records.csv`

  * Model-level performance across FS–FE–Classifier combinations
  * Includes **Δ Macro-F1** to quantify performance changes

## 📌 Key Highlights

* **LDA consistently provides the strongest performance** across all datasets
* **Stacking ensemble (STACK)** achieves the best overall classification results
* **FS→FE interactions are synergistic**, not merely additive
* **PCA may degrade performance**, especially on smaller datasets (e.g., AWID)
* Larger datasets (UNSW, CIC) benefit significantly from **supervised feature extraction (LDA)**

## ⚠️ Note on Code Availability

The repository currently provides **complete experimental results** to support transparency and reproducibility of the reported findings.

👉 The **source code and full implementation details will be released after the acceptance of the manuscript**.


* tailor this README for **IEEE / Elsevier style**
* or create a **short “GitHub summary version” + detailed “docs/README_full.md” split** (which reviewers love)
