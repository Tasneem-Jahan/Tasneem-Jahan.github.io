---
title: "B.Sc. Thesis Defense: Heart Disease Prediction Using Machine Learning"
collection: talks
type: "Undergraduate Thesis Defense Presentation"
permalink: /talks/2023-07-heart-disease-defense/
venue: "Department of Computer Science, American International University-Bangladesh (AIUB)"
date: 2023-05-22
location: "Dhaka, Bangladesh"
---

<div class="pub-citation">
  <strong>Tasneem Jahan Farheen</strong>, Zuaina Zabin Shera, S.M. Hasanuzzaman Abir, Muntasir Rahman<br>
  <em>Supervised by Tanvir Ahmed</em> — American International University-Bangladesh (AIUB), July 2023 
</div>

<div class="research-tags">
  <span class="research-tag">Support Vector Machine (SVM)</span>
  <span class="research-tag">K-Nearest Neighbors</span>
  <span class="research-tag">10-Fold Cross-Validation</span>
  <span class="research-tag">Clinical Informatics</span>
  <span class="research-tag">AIUB CSE</span>
</div>

<div class="pub-actions">
  <a href="/research/heart-disease-prediction/">
    <i class="fas fa-book-open"></i> Full Research Overview
  </a>
</div>

---

### Presentation Overview

Cardiovascular disease remains the leading global cause of mortality and morbidity. Clinical detection is complicated by the lack of a single definitive diagnostic test, often requiring doctors to synthesize multiple laboratory and physiological indicators.

This defense presentation outlines our undergraduate thesis, which addressed data scarcity and single-source bias by combining five standard benchmarks with the Z-Alizadeh Sani clinical registry. We evaluated five supervised classification algorithms through 10-fold cross-validation and hyperparameter optimization to select an accurate, generalizable, and clinical-ready screening model.

<div style="display: flex; flex-direction: row; align-items: center; justify-content: space-between; gap: 8px; margin: 24px 0; padding: 16px; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 10px; width: 100%; box-sizing: border-box; overflow-x: auto;">
  
  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-heartbeat"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Clinical Need</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Early Triage & Diagnosis</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-layer-group"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Cohort Merging</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">1,219 Filtered Samples</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-chart-line"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Model Selection</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">10-Fold CV & ROC-AUC</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-user-md"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Best Classifier</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">SVM: 88.99% Recall</div>
  </div>

</div>

---

### Defense Presentation Roadmap

1. **Introduction & Motivation:** The burden of cardiovascular diseases, early risk indicators, and the motivation to build automated risk-assessment tools for clinicians.
2. **Related Literature:** Reviewing deep learning ECG models, hybrid random forests (HRFLM), and traditional classification benchmarks.
3. **Data Engineering & Harmonization:** Merging the UCI multi-cohort database with the Z-Alizadeh Sani dataset, standardizing 8 physiological features, Min-Max scaling, and deduplicating down to 1,219 patient instances.
4. **Experimental Setup:** 10-fold cross-validation architecture, hyperparameter optimization (k = 15 for KNN), and evaluation metrics focusing on accuracy, precision, sensitivity, and F1-score.
5. **Results & Model Selection:** Overfitting diagnosis of Random Forest, ROC-AUC comparison between KNN (0.7480) and SVM (0.8031), and hold-out test set performance.
6. **Clinical Implications & Future Scope:** Prioritizing false-negative reduction and laying the groundwork for clinical screening software integration.

---

### Core Defense Findings & Results Summary

* **SVM Selected as the Best Performing Classifier:**
  * While KNN and Random Forest scored competitive validation accuracy (~80.31%), SVM achieved superior generalization stability and a higher ROC-AUC (0.8031 vs. 0.7480).
  * On the 70/30 hold-out test evaluation, SVM achieved **81.97% accuracy**, **82.20% precision**, **88.99% sensitivity (recall)**, and an **85.46% F1-score**.
* **Rejection of Overfitted Models:**
  * Random Forest achieved a 100% score across all training metrics but dropped to 80.31% validation accuracy, indicating significant memorization of training data.
* **Clinical Significance of High Sensitivity:**
  * With only 24 false negatives against 194 true positives in the test split, the SVM model minimizes life-threatening diagnostic omissions.
