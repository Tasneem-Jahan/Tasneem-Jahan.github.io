---
title: "Knowledge Distillation in Split Learning for Clinical Tabular Data"
excerpt: "A split learning framework with logit-level and encoder-level knowledge distillation for heterogeneous clinical tabular datasets."
collection: research
permalink: /research/knowledge-distillation-split-learning/
date: 2026-03-11
---

<div class="pub-citation">
  <strong>Tasneem Jahan Farheen</strong> (Supervised by Dr. Md. Golam Rabiul Alam)<br>
  <em>Master of Science in Computer Science and Engineering Thesis</em> — BRAC University, March 2026 
</div>

<div class="research-tags">
  <span class="research-tag">Split Learning</span>
  <span class="research-tag">Knowledge Distillation</span>
  <span class="research-tag">Tabular Deep Learning</span>
  <span class="research-tag">Few-Shot Learning</span>
  <span class="research-tag">Healthcare AI</span>
  <span class="research-tag">PyTorch</span>
</div>

<div class="pub-actions">
  <a href="https://dspace.bracu.ac.bd/items/fcb0c1f9-183f-4bd4-aba8-3f915c5e4c58" target="_blank" rel="noopener">
    <i class="fas fa-file-pdf"></i> Read Full Thesis (DSpace)
  </a>
  <a href="/talks/2026-03-defense-talk/">
    <i class="fas fa-chalkboard-teacher"></i> Defense Slides
  </a>
  <a href="/publication/2026-03-04-split-learning-thesis/">
    <i class="fas fa-book-open"></i> Publication Entry
  </a>
</div>

---

### Project Overview

Predictive machine learning models in healthcare often struggle with data decentralization and strict governance regulations that prohibit the pooling of raw patient records across hospital networks. Additionally, target clinics in resource-constrained settings frequently suffer from limited labeled records. 

This research introduces a privacy-preserving framework combining **Split Learning (SL)** with **Knowledge Distillation (KD)** for diabetes risk prediction across heterogeneous clinical tabular datasets. High-capacity teacher models are trained across distributed source cohorts without data centralization, subsequently transferring structured predictive knowledge to compact student models deployed in data-scarce target environments.

<div style="display: flex; flex-direction: row; align-items: center; justify-content: space-between; gap: 8px; margin: 24px 0; padding: 16px; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 10px; width: 100%; box-sizing: border-box; overflow-x: auto;">
  
  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-hospital-user"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Source Silos</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">NHANES & HRS</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-network-wired"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Split Learning</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Smash Data Exchange</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-brain"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Distillation Transfer</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Logit & Encoder KD</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-notes-medical"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Target Deployment</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Few-Shot (Pima & Sylhet)</div>
  </div>

</div>

---

### Key Highlights & Technical Contributions

* **Decentralized Privacy-Preserving Architecture:** Partitions neural network layers between local client institutions and a shared server backbone. Raw patient records remain strictly local, exchanging only intermediate activations (smash data) and gradients across the privacy boundary.
* **Dual Knowledge Distillation Paradigms:**
  * **Logit-Level KD (Framework 1):** Transfers soft probability distributions from the split-learning teacher to establish stabilized decision boundaries under sparse supervision.
  * **Encoder-Level KD (Framework 2):** Aligns intermediate latent representations using Mean Squared Error (MSE) loss to transfer structural feature dependencies across institutional distributions.
* **Extreme Few-Shot Supervision Protocol:** Rigorously evaluates model adaptation under extreme sample scarcity with balanced subsets of K in {5, 10, 20} labeled samples per class, treating remaining records as unlabeled transfer data.
* **Cross-Architecture Benchmarking:** Evaluates three distinct student model families—standard feed-forward networks (**MLP**), attention-based tabular transformers (**SAINT**), and batch-ensemble networks (**TabM**).
* **Multi-Cohort Heterogeneous Validation:** Benchmarked across distinct clinical cohorts, evaluating cross-domain shifts across laboratory-measured populations (NHANES, HRS, Pima) and a 520-patient symptom-based clinical cohort from Sylhet, Bangladesh.

---

### Empirical Evaluation & Results Summary

#### Pima Primary Target Cohort (K = 5 Samples Per Class)
Under severe data scarcity (K = 5), distillation provides substantial performance and calibration gains across 5 independent random seeds:

| Student Model | Training Regime | ROC-AUC (mean ± std) | PR-AUC (mean ± std) | Calibrated Brier (lower is better) |
| :--- | :--- | :--- | :--- | :--- |
| **MLP** | Scratch Baseline | 0.7028 ± 0.0574  | 0.5800 ± 0.1047  | 0.2140 ± 0.0237  |
| **MLP** | Logit-Level KD (F1) | **0.7894 ± 0.0106**  | **0.7126 ± 0.0187**  | **0.1770 ± 0.0113**  |
| **MLP** | Encoder-Level KD (F2) | 0.7597 ± 0.0233  | 0.6538 ± 0.0228  | 0.1871 ± 0.0068  |
| **TabM** | Scratch Baseline | 0.6314 ± 0.1104  | 0.5379 ± 0.1402  | 0.2408 ± 0.0236  |
| **TabM** | Logit-Level KD (F1) | **0.7923 ± 0.0132**  | **0.7201 ± 0.0228**  | **0.1835 ± 0.0088**  |
| **TabM** | Encoder-Level KD (F2) | 0.7525 ± 0.0203  | 0.6280 ± 0.0239  | 0.1916 ± 0.0079  |
| **SAINT** | Scratch Baseline | 0.7688 ± 0.0492  | 0.6234 ± 0.0551  | 0.2022 ± 0.0093  |
| **SAINT** | Logit-Level KD (F1) | 0.7623 ± 0.0451  | **0.6781 ± 0.0518**  | **0.1882 ± 0.0146**  |

#### Core Takeaways
* **Inductive Bias vs. Distillation:** Architectures lacking specialized tabular priors (MLP and TabM) benefit most substantially from teacher guidance, showing ROC-AUC improvements up to +16.09% . Conversely, SAINT demonstrates saturation due to its inherent attention-based inductive priors .
* **Discrimination vs. Calibration Trade-Off:** Logit-level transfer primarily drives discriminative ranking (ROC-AUC), whereas encoder-level feature alignment consistently yields superior probabilistic calibration (BrierCal) and minimizes prediction variance across heterogeneous domains .
* **Clinical Screening Reliability:** On the Sylhet cohort, distillation reduced false negatives at threshold 0.5, raising test recall from 0.7417 to 0.8792 for MLP at K = 5 while lowering calibration error by up to 33% .
