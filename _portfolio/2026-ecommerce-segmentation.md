---
title: "E-Commerce Customer Segmentation & RFM Clustering"
excerpt: "Unsupervised machine learning pipeline combining RFM feature engineering, PCA dimensionality reduction, and K-Means clustering to identify high-value customer cohorts."
collection: portfolio
permalink: /portfolio/2026-ecommerce-segmentation/
date: 2026-07-20
---

<div class="pub-citation">
  <strong>Tasneem Jahan Farheen</strong><br>
  <em>Unsupervised Machine Learning, Behavioral Clustering & Customer Analytics</em> — July 2026
</div>

<div class="research-tags">
  <span class="research-tag">Python</span>
  <span class="research-tag">Unsupervised Learning</span>
  <span class="research-tag">K-Means Clustering</span>
  <span class="research-tag">PCA</span>
  <span class="research-tag">RFM Analysis</span>
  <span class="research-tag">Scikit-Learn</span>
</div>

<div class="pub-actions">
  <a href="https://github.com/Tasneem-Jahan/rfm-customer-segmentation-engine" target="_blank" rel="noopener">
    <i class="fab fa-github"></i> View GitHub Repository
  </a>
  <a href="#clustering-workflow">
    <i class="fas fa-project-diagram"></i> Architecture
  </a>
  <a href="#cluster-profiles">
    <i class="fas fa-users"></i> Customer Personas
  </a>
</div>

---

### Project Overview

This project implements an end-to-end unsupervised customer segmentation pipeline for transactional e-commerce data. By synthesizing high-dimensional purchase histories into behavioral **RFM (Recency, Frequency, Monetary)** representations, the model applies **Principal Component Analysis (PCA)** and **K-Means clustering** to discover distinct, actionable customer archetypes for retention marketing and targeted campaigns.

<div style="display: flex; flex-direction: row; align-items: center; justify-content: space-between; gap: 8px; margin: 24px 0; padding: 16px; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 10px; width: 100%; box-sizing: border-box; overflow-x: auto;">
  
  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-receipt"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Transaction Logs</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Invoices & Items</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-filter"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">RFM Engineering</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Log Transforms & Scale</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-braille"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">PCA & K-Means</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Silhouette Tuning</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-bullseye"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Cohorts & Personas</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Targeted Strategy</div>
  </div>

</div>

---

<h3 id="clustering-workflow">Technical Highlights & Pipeline Design</h3>

* **Data Cleaning & Preprocessing:**
  * Cleaned transactional logs by filtering canceled orders, handling negative return quantities, and removing missing customer identifiers.
  * Extracted granular features including basket diversity, unit revenue per transaction, and geographic distributions.
* **Feature Engineering & Transformation:**
  * Aggregated raw invoice logs into customer-level **RFM** features:
    * **Recency:** Days elapsed since last recorded order.
    * **Frequency:** Total unique purchase transactions over the study period.
    * **Monetary Value:** Net cumulative revenue generated per customer account.
  * Corrected heavy right-skewed revenue and order distributions using logarithmic transformations (`np.log1p`) followed by standard z-score normalization (`StandardScaler`).
* **Dimensionality Reduction & Clustering Optimization:**
  * Utilized **Principal Component Analysis (PCA)** to capture $>80\%$ of variance while mitigating collinearity between frequency and total expenditure.
  * Evaluated cluster stability and optimal $k$ selection using the **Elbow Method (Inertia)** and **Silhouette Coefficient Analysis**.

---

<h3 id="cluster-profiles">Discovered Customer Cohorts</h3>

| Cohort | Characteristics | Behavioral Profile | Strategic Intervention |
| :--- | :--- | :--- | :--- |
| **High-Value Champions** | Low Recency, High Frequency, High Spend | Core advocates contributing majority gross margins | VIP loyalty rewards, early product access |
| **Loyal Repeaters** | Low Recency, Moderate Frequency, Steady Spend | Consistent periodic purchasing cadence | Upselling, cross-selling bundle recommendations |
| **At-Risk / Slipping** | High Recency, High Historic Spend, Zero Recent Orders | Formerly high-value buyers showing churn signals | Re-engagement discounts, feedback surveys |
| **Low-Engagement Occasionals** | High Recency, Single Order, Low Basket Value | One-time discount or seasonal shoppers | Automated win-back campaigns, low-cost newsletters |

---

### Tech Stack

| Layer | Tools | Responsibility |
| :--- | :--- | :--- |
| **Environment** | Python, Jupyter Notebook | Data exploration, feature prototyping |
| **Manipulation** | Pandas, NumPy | Aggregations, matrix operations, log transformations |
| **Machine Learning** | Scikit-Learn | K-Means, PCA, StandardScaler, Silhouette Metrics |
| **Visualization** | Seaborn, Matplotlib | Radar plots, 2D/3D cluster scatter plots, Elbow curves |
