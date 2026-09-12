---
title: "Heart Disease Prediction Using Machine Learning"
excerpt: "A comparative clinical tabular study benchmarked across merged multi-center cohorts (UCI and Kaggle) using 10-fold cross-validation and hyperparameter optimization."
collection: research
permalink: /research/heart-disease-prediction/
date: 2023-07-12
---

<div class="pub-citation">
  <strong>Tasneem Jahan Farheen</strong>, Zuaina Zabin Shera, S.M. Hasanuzzaman Abir, Muntasir Rahman (Supervised by Tanvir Ahmed)<br>
  <em>Bachelor of Science in Computer Science and Engineering Thesis</em> — American International University-Bangladesh (AIUB), July 2023 [1]
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
  <a href="/talks/2023-07-heart-disease-defense/">
    <i class="fas fa-chalkboard-teacher"></i> Defense Presentation & Slides
  </a>
  <a href="https://github.com/Tasneem-Jahan" target="_blank" rel="noopener">
    <i class="fab fa-github"></i> Code Repository
  </a>
  <a href="#methodology-workflow">
    <i class="fas fa-project-diagram"></i> Methodology
  </a>
  <a href="#empirical-benchmarks">
    <i class="fas fa-chart-bar"></i> Results & Benchmarks
  </a>
</div>

---

### Project Overview

Cardiovascular diseases (CVDs) remain the leading cause of mortality worldwide, responsible for an estimated 700,000 deaths annually [1]. Timely clinical diagnosis is often hindered by heterogeneous feature sets and non-standardized diagnostic criteria across institutions [1, 2].

This study evaluates five supervised machine learning models across a harmonized, multi-center clinical dataset created by merging five international cohorts (Cleveland, Hungarian, Switzerland, Long Beach VA, and Statlog) with the Z-Alizadeh Sani clinical registry [1]. Using a standardized 10-fold cross-validation protocol and ROC-AUC analysis, the framework assesses generalization ability and prioritizes the reduction of critical false negatives in clinical triage [1].

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
  * Merged 1,763 initial patient records from the UCI Machine Learning Repository and Kaggle benchmarks [1].
  * Re-engineered and aligned disparate feature definitions from the 54-attribute Z-Alizadeh Sani dataset to match the 12-attribute comprehensive baseline [1]:
    * **Derived Chest Pain (`cp`):** Standardized typical angina (1), atypical angina (2), non-anginal pain (3), and asymptomatic presentations (0) [1].
    * **Derived Serum Cholesterol (`chol`):** Formulated from clinical components via total cholesterol calculation: $\text{HDL} + \text{LDL} + 0.20 \times \text{Triglycerides}$ [1].
    * **Derived Rest ECG (`restecg`):** Mapped ST elevation, ST depression, T-wave inversion (coded as 1), and left ventricular hypertrophy (coded as 2) [1].
* **Data Cleaning & Scaling:**
  * Deduplicated records, yielding a final leak-free corpus of **1,219 complete observations** across 8 standardized predictors (`Age`, `Sex`, `cp`, `BP`, `Chol`, `FBS`, `ecg`, `exang`) and the binary diagnosis target (`num`) [1, 2].
  * Scaled continuous physiological measures (`Age`, `BP`, `Chol`) using Min-Max Normalization and standardized training folds prior to classification [1].
* **Validation Protocol & Model Benchmarking:**
  * Evaluated five distinct classifier paradigms: **Support Vector Machines (SVM)**, **K-Nearest Neighbors (KNN)**, **Random Forest**, **Logistic Regression**, and **Gaussian Naive Bayes** [1].
  * Emphasized 10-fold cross-validation across all iterations to prevent sample partition bias [1].

---

### Key Empirical Findings & Conclusions (Heart Disease Study)

* **Cross-Validation Stability:** SVM and KNN demonstrated the closest alignment between training and validation scores, avoiding the variance issues seen in other models[cite: 2, 3].
* **Rejection of Overfitting:** Random Forest attained 100% training performance across all metrics but dropped to 80.31% validation accuracy, demonstrating severe memorization of noise rather than generalizable clinical patterns[cite: 2, 3].
* **ROC-AUC Discriminative Advantage:** Between the top candidates, SVM showed superior boundary discrimination over KNN, achieving a higher AUC (0.8031 vs. 0.7480)[cite: 2, 3].
* **High Clinical Sensitivity:** On the 70/30 hold-out test set, the final SVM model attained an 88.99% recall (sensitivity) with only 24 false negatives against 194 true positives[cite: 2, 3].
* **Mitigating Life-Threatening Omissions:** Minimizing Type-2 errors is critical in cardiac diagnostics, as failing to identify an at-risk patient carries severe medical consequences compared to false alarms[cite: 2].
* **Balanced Overall Diagnostics:** SVM maintained robust, well-rounded test metrics with 81.97% accuracy, 82.20% precision, and an 85.46% F1-score across diverse multi-center records[cite: 2, 3].

### Key Findings & Clinical Takeaways

* **Minimizing False Negatives in Triage:** In cardiac diagnostics, Type-2 errors (false negatives) carry severe clinical risk by depriving at-risk patients of critical monitoring [1]. The tuned SVM model achieved an 88.99% recall on the hold-out test set, minimizing missed diagnoses [1].
* **Overfitting Diagnostics:** Random Forest achieved 100% training accuracy across all folds but degraded to 80.31% on validation, indicating an inability to generalize beyond cohort-specific noise [1]. Conversely, SVM maintained tight consistency between training (83.24%) and validation (80.23%) [1].
* **Harmonized Multi-Center Reliability:** Integrating multiple international cohorts eliminated single-center sampling bias, establishing a robust clinical risk pipeline across diverse demographic groups [1].
