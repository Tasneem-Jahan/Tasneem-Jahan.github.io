---
title: "Heart Disease Prediction Using Machine Learning"
excerpt: "A comparative clinical tabular study benchmarked across merged multi-center cohorts (UCI and Kaggle) using 10-fold cross-validation and hyperparameter optimization."
collection: research
permalink: /research/heart-disease-prediction/
date: 2023-05-22
---

<div class="pub-citation">
  <strong>Tasneem Jahan Farheen</strong>, Zuaina Zabin Shera, S.M. Hasanuzzaman Abir, Muntasir Rahman (Supervised by Tanvir Ahmed)<br>
  <em>Bachelor of Science in Computer Science and Engineering Thesis</em> — American International University-Bangladesh (AIUB), May 2023
</div>

<div class="research-tags">
  <span class="research-tag">Support Vector Machine (SVM)</span>
  <span class="research-tag">K-Nearest Neighbors (KNN)</span>
  <span class="research-tag">10-Fold Cross-Validation</span>
  <span class="research-tag">Clinical Risk Prediction</span>
  <span class="research-tag">Tabular Preprocessing</span>
  <span class="research-tag">Scikit-Learn</span>
</div>

<div class="pub-actions">
  <a href="/talks/2023-05-heart-disease-defense/">
    <i class="fas fa-chalkboard-teacher"></i> Defense Presentation
  </a>
</div>

---

### Project Overview

Cardiovascular diseases (CVDs) remain the leading cause of mortality worldwide, responsible for an estimated 700,000 deaths annually. Timely clinical diagnosis is often hindered by heterogeneous feature sets and non-standardized diagnostic criteria across institutions.

This study evaluates five supervised machine learning models across a harmonized, multi-center clinical dataset created by merging five international cohorts (Cleveland, Hungarian, Switzerland, Long Beach VA, and Statlog) with the Z-Alizadeh Sani clinical registry. Using a standardized 10-fold cross-validation protocol and ROC-AUC analysis, the framework assesses generalization ability and prioritizes the reduction of critical false negatives in clinical triage.

<div style="display: flex; flex-direction: row; align-items: center; justify-content: space-between; gap: 8px; margin: 24px 0; padding: 16px; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 10px; width: 100%; box-sizing: border-box; overflow-x: auto;">
  
  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-database"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Merged Cohorts</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">UCI & Kaggle Sources</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-filter"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Harmonization</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">MinMax & Deduplication</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-sync-alt"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">10-Fold CV</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Hyperparameter Tuning</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-heartbeat"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">SVM Prediction</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">High Sensitivity Focus</div>
  </div>

</div>

---

<h3 id="methodology-workflow">Technical Methodology & Cohort Preparation</h3>

* **Multi-Source Dataset Harmonization:**
  * Merged 1,763 initial patient records from the UCI Machine Learning Repository and Kaggle benchmarks.
  * Re-engineered and aligned disparate feature definitions from the 54-attribute Z-Alizadeh Sani dataset to match the 12-attribute comprehensive baseline:
    * **Derived Chest Pain (cp):** Standardized typical angina (1), atypical angina (2), non-anginal pain (3), and asymptomatic presentations (0).
    * **Derived Serum Cholesterol (chol):** Formulated from clinical components via total cholesterol calculation: HDL + LDL + 20% triglycerides.
    * **Derived Rest ECG (restecg):** Mapped ST elevation, ST depression, T-wave inversion (coded as 1), and left ventricular hypertrophy (coded as 2).
* **Data Cleaning & Scaling:**
  * Deduplicated records, yielding a final leak-free corpus of **1,219 complete observations** across 8 standardized predictors (Age, Sex, cp, BP, Chol, FBS, ecg, exang) and the binary diagnosis target (num).
  * Scaled continuous physiological measures (Age, BP, Chol) using Min-Max Normalization and standardized training folds prior to classification.
* **Validation Protocol & Model Benchmarking:**
  * Evaluated five distinct classifier paradigms: **Support Vector Machines (SVM)**, **K-Nearest Neighbors (KNN)**, **Random Forest**, **Logistic Regression**, and **Gaussian Naive Bayes**.
  * Emphasized 10-fold cross-validation across all iterations to prevent sample partition bias.

---

### Key Empirical Findings & Conclusions

* **Cross-Validation Stability:** SVM and KNN demonstrated the closest alignment between training and validation scores, avoiding the variance issues seen in other models.
* **Rejection of Overfitting:** Random Forest attained 100% training performance across all metrics but dropped to 80.31% validation accuracy, demonstrating severe memorization of noise rather than generalizable clinical patterns.
* **ROC-AUC Discriminative Advantage:** Between the top candidates, SVM showed superior boundary discrimination over KNN, achieving a higher AUC (0.8031 vs. 0.7480).
* **High Clinical Sensitivity:** On the 70/30 hold-out test set, the final SVM model attained an 88.99% recall (sensitivity) with only 24 false negatives against 194 true positives.
* **Mitigating Life-Threatening Omissions:** Minimizing Type-2 errors is critical in cardiac diagnostics, as failing to identify an at-risk patient carries severe medical consequences compared to false alarms.
* **Balanced Overall Diagnostics:** SVM maintained robust, well-rounded test metrics with 81.97% accuracy, 82.20% precision, and an 85.46% F1-score across diverse multi-center records.
