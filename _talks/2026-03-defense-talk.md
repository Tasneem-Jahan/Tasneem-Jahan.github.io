---
title: "M.Sc. Thesis Defense: Knowledge Distillation in Split Learning for Heterogeneous Clinical Tabular Data"
collection: talks
type: "Oral Defense Presentation"
permalink: /talks/2026-03-defense-talk
venue: "Department of Computer Science and Engineering, BRAC University"
date: 2026-03-11
location: "Dhaka, Bangladesh"
---

<div class="pub-citation">
  <strong>Tasneem Jahan Farheen</strong> (Supervised by Dr. Md. Golam Rabiul Alam)<br>
  <em>Master of Science in Computer Science and Engineering Oral Defense</em> — BRAC University, March 2026 
</div>

<div class="research-tags">
  <span class="research-tag">Split Learning</span>
  <span class="research-tag">Knowledge Distillation</span>
  <span class="research-tag">Few-Shot Supervision</span>
  <span class="research-tag">Tabular Deep Learning</span>
  <span class="research-tag">Healthcare AI</span>
</div>

<div class="pub-actions">
  <a href="https://dspace.bracu.ac.bd/items/fcb0c1f9-183f-4bd4-aba8-3f915c5e4c58" target="_blank" rel="noopener">
    <i class="fas fa-file-pdf"></i> Read Full Thesis (DSpace)
  </a>
  <a href="/publications/2026-03-11-split-learning-thesis">
    <i class="fas fa-book-open"></i> Publication Entry
  </a>
</div>

---

### Presentation Overview

Clinical datasets across hospital networks remain heavily fragmented due to strict data privacy regulations (e.g., HIPAA, GDPR) that prohibit centralizing patient records. Concurrently, small or resource-limited healthcare institutions face severe label scarcity where obtaining annotated clinical examples is difficult and costly.

This thesis defense introduces a framework integrating **Split Learning (SL)** with two distinct **Knowledge Distillation (KD)** pathways:
1. **Framework 1 (Logit-Level KD):** Distills decision boundary uncertainty from a split-learning teacher using soft probabilities.
2. **Framework 2 (Encoder-Level KD):** Enforces latent representation alignment via feature-space Mean Squared Error (MSE) loss.

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
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Smash Activations Exchange</div>
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
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Pima (K in {5, 10, 20})</div>
  </div>

</div>

---

### Key Research Questions Addressed

* **Q1 (Collaborative AI):** Can split learning enable effective cross-domain knowledge transfer without sharing raw clinical records across institutions?
* **Q2 (Few-Shot Discrimination):** Does logit-level distillation improve predictive discrimination when labeled samples are extremely limited?
* **Q3 (Representation Alignment & Calibration):** Does encoder-level distillation improve feature geometry robustness and probability calibration under institutional domain shifts?
* **Q4 (Depth of Transfer Dynamics):** How does the layer depth of knowledge transfer govern the trade-off between discrimination ranking and uncertainty calibration?

---

### Core Findings & Defense Conclusions

* **Substantial Lift Under Extreme Starvation (K = 5):**
  * Logit-level distillation produced large ranking gains for architectures without tabular inductive biases, elevating **MLP ROC-AUC from 0.7028 to 0.7894** and **TabM ROC-AUC from 0.6314 to 0.7923**.
* **Consistent Calibration Reliability:**
  * Both distillation strategies consistently lowered the calibrated Brier score across student models, reducing overconfident errors under cross-domain distribution shifts.
* **Supervision Scaling Dynamics:**
  * Distillation gains are greatest under extreme few-shot regimes (K = 5) and gradually diminish as target supervision increases (K = 10, 20), confirming that teacher knowledge acts primarily as an effective low-resource regularizer.
* **Architecture-Specific Sensitivity:**
  * While MLP and TabM gained marked improvements, **SAINT** exhibited saturation (ROC-AUC 0.7688 scratch vs. 0.7623 KD at K = 5) because its self-attention and inter-sample attention mechanisms already capture robust geometric relationships from tabular inputs.
* **Transfer Trade-Off:**
  * Logit-level transfer primarily optimizes decision ranking and discriminative boundary separation, whereas encoder-level latent alignment prioritizes calibration consistency and feature stability.

