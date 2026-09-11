---
title: "Knowledge Distillation in Split Learning for Heterogeneous Clinical Tabular Data"
collection: publications
category: "thesis"
permalink: /publication/2026-03-04-split-learning-thesis
date: 2026-03-04
venue: 'BRAC University Institutional Repository (DSpace)'
tags:
  - Split Learning
  - Knowledge Distillation
  - Tabular Deep Learning
  - Few-Shot Learning
  - Healthcare AI
  - PyTorch
---

<div class="pub-citation">
  <strong>Tasneem Jahan Farheen</strong> (Supervised by Dr. Md. Golam Rabiul Alam)<br>
  <em>Master of Science in Computer Science and Engineering Thesis</em> — BRAC University Institutional Repository (DSpace), March 2026
</div>

<div class="research-tags">
  <span class="research-tag">Split Learning</span>
  <span class="research-tag">Knowledge Distillation</span>
  <span class="research-tag">FT-Transformer</span>
  <span class="research-tag">SAINT</span>
  <span class="research-tag">TabM</span>
  <span class="research-tag">Few-Shot Supervision</span>
</div>

<div class="pub-actions">
  <a href="https://dspace.bracu.ac.bd/items/fcb0c1f9-183f-4bd4-aba8-3f915c5e4c58" target="_blank" rel="noopener">
    <i class="fas fa-file-pdf"></i> Download Full Thesis (DSpace)
  </a>
  <a href="https://github.com/Tasneem-Jahan" target="_blank" rel="noopener">
    <i class="fab fa-github"></i> Code Repository
  </a>
  <a href="/talks/2026-03-defense-talk/">
    <i class="fas fa-chalkboard-teacher"></i> Defense Presentation
  </a>
  <a href="#citation">
    <i class="fas fa-quote-right"></i> Cite (BibTeX)
  </a>
</div>

---

### Core Research Contributions

* **Privacy-Preserving Cross-Silo Collaboration:** Introduces a decentralized framework that decouples tabular feature encoders from a shared server backbone, ensuring patient-level tabular records never leave institutional boundaries while transmitting only intermediate representations (smash data).
* **Dual Knowledge Distillation Paradigms:** Systematically formulates and contrasts two transfer pathways from a collaborative FT-Transformer teacher: **Logit-Level KD** (soft predictive decision boundaries) and **Encoder-Level KD** (latent latent-space alignment via MSE).
* **Extreme Few-Shot Robustness ($K \in \{5, 10, 20\}$):** Demonstrates that teacher guidance offsets severe sample scarcity, improving discriminative power up to $+16.09\%$ in ROC-AUC for capacity-constrained architectures at $K=5$.
* **Decoupled Discrimination vs. Calibration Dynamics:** Uncovers that logit-level transfer primarily optimizes decision ranking (ROC-AUC), whereas encoder-level alignment drives model reliability by substantially reducing Expected Calibration Error and Brier scores under cross-domain distribution shifts.
* **Multi-Cohort Heterogeneous Validation:** Validated across distinct feature modalities—bridging continuous laboratory measurements (NHANES, HRS, Pima) and pure symptom-based binary clinical profiles (Sylhet 520-cohort).

---

### Abstract

The growing availability of clinical data across institutions creates new opportunities for improved disease risk prediction. However, privacy regulations, institutional policies, and limited labeled data restrict centralized model training, particularly in low-resource settings. To address these challenges, this study presents a privacy-preserving framework that integrates split learning and knowledge distillation for diabetes risk prediction using heterogeneous tabular datasets. 

This work systematically evaluates two complementary transfer mechanisms:
1. **Logit-Level Knowledge Distillation:** Transfers predictive decision boundaries from high-capacity teacher models, collaboratively trained on large population datasets (NHANES and HRS), to lightweight student models in low-resource target domains.
2. **Encoder-Level Knowledge Distillation:** Aligns latent feature representations within a split learning architecture using mean squared error feature matching.

Both approaches maintain strict data privacy by keeping raw patient data local and exchanging only intermediate activations. Experimental results under few-shot supervision indicate that logit-level distillation substantially improves discriminative performance, particularly in extremely low-label scenarios, while stabilizing training across heterogeneous domains. Encoder-level distillation further improves probabilistic calibration and representation alignment under cross-domain distribution shifts. These findings underscore the significance of structured knowledge transfer in privacy-preserving clinical machine learning and offer practical recommendations for deploying reliable models in heterogeneous healthcare environments.

---

### Methodological Architecture

The proposed system operates across three decoupled phases:

1. **Stage 1 — Split Teacher Pretraining (Source Silos):** A high-capacity **FT-Transformer** (128 hidden dim, 4 attention heads, 3 transformer layers) is collaboratively trained across distinct institutional clients (NHANES and HRS). Private client encoders extract embeddings locally, transmitting smash data across the privacy boundary to a shared server backbone.
2. **Stage 2 — Target Adaptation via Knowledge Distillation:** Lightweight student models (**MLP**, **SAINT**, and **TabM**) adapt to target clinics under balanced few-shot supervision ($K=5, 10, 20$ samples per class). Unlabeled target samples receive guidance via either soft probability loss ($\mathcal{L}_{\text{KD}}$) or latent activation matching ($\mathcal{L}_{\text{align}}$).
3. **Stage 3 — Evaluation & Post-Hoc Calibration:** Benchmarked across 5 independent seeds on held-out test splits using threshold-independent discrimination (ROC-AUC, PR-AUC), threshold-level metrics at $\tau=0.5$, and validation-fitted temperature scaling for calibrated Brier score analysis ($\text{BrierCal}$).

---

### Key Empirical Findings

#### 1. Primary Target Domain: Pima Indians Diabetes Benchmark (Lab Measurements)
Under severe label starvation ($K=5$), teacher-guided knowledge transfer dramatically stabilizes student architectures lacking specialized tabular inductive biases:

| Architecture | Training Regime | ROC-AUC (mean ± std) | PR-AUC (mean ± std) | Calibrated Brier ($\downarrow$) |
| :--- | :--- | :--- | :--- | :--- |
| **MLP** | Scratch Baseline ($K=5$) | $0.7028 \pm 0.0574$ | $0.5800 \pm 0.1047$ | $0.2140 \pm 0.0237$ |
| **MLP** | Logit-Level KD ($K=5$) | **$0.7894 \pm 0.0106$** | **$0.7126 \pm 0.0187$** | **$0.1770 \pm 0.0113$** |
| **MLP** | Encoder-Level KD ($K=5$) | $0.7597 \pm 0.0233$ | $0.6538 \pm 0.0228$ | $0.1871 \pm 0.0068$ |
| **TabM** | Scratch Baseline ($K=5$) | $0.6314 \pm 0.1104$ | $0.5379 \pm 0.1402$ | $0.2408 \pm 0.0236$ |
| **TabM** | Logit-Level KD ($K=5$) | **$0.7923 \pm 0.0132$** | **$0.7201 \pm 0.0228$** | **$0.1835 \pm 0.0088$** |
| **TabM** | Encoder-Level KD ($K=5$) | $0.7525 \pm 0.0203$ | $0.6280 \pm 0.0239$ | $0.1916 \pm 0.0079$ |
| **SAINT** | Scratch Baseline ($K=5$) | $0.7688 \pm 0.0492$ | $0.6234 \pm 0.0551$ | $0.2022 \pm 0.0093$ |
| **SAINT** | Logit-Level KD ($K=5$) | $0.7623 \pm 0.0451$ | **$0.6781 \pm 0.0518$** | **$0.1882 \pm 0.0146$** |

*Note: SAINT exhibits an architectural saturation effect—because its self-attention and inter-sample attention mechanisms already capture robust geometric relationships from tabular tokens, additional distillation yields marginal discriminative gain.*

#### 2. Cross-Modality Target Domain: Sylhet Clinical Cohort (Symptom Records)
To test cross-modality domain shift, the framework was evaluated on the 520-patient Sylhet dataset (comprising 15 binary clinical symptoms and 1 continuous feature). 

* **Consistent Reliability Gains:** Even though symptom features provide high baseline discriminability (scratch models reaching $>0.91$ ROC-AUC), knowledge distillation drove consistent probability calibration improvements across all settings.
* **Calibration Error Reduction:** For MLP ($K=5$), encoder-level alignment reduced $\text{BrierCal}$ from $0.1600$ to $0.1076$ (a **$33\%$ error reduction**). At $K=20$, TabM under encoder distillation achieved the lowest overall calibration error ($\text{BrierCal} = 0.0880$).
* **Mitigating Clinical False Negatives:** At an operational cutoff of $\tau=0.5$, logit distillation reduced missed diabetic diagnoses, boosting MLP test recall from $0.7417$ to $0.8792$.

---

### Experimental Setup & Hyperparameters

* **Teacher Backbone:** FT-Transformer (128 embedding dim, 4 heads, 3 layers, dropout 0.1, ReLU).
* **Student Architectures:** Standard MLP (2–3 layers, 128 dim, dropout 0.2), SAINT (2 transformer layers, 4 heads, 128 dim), and TabM (Small BatchEnsemble variant, 128 dim).
* **Optimization:** Adam optimizer, learning rate $\eta = 1 \times 10^{-3}$, weight decay $1 \times 10^{-5}$, batch size 32, validation patience of 10 epochs.
* **Loss Trade-offs:** Framework 1 balances supervised and logit loss with $\alpha = 0.5$[cite: 1]; Framework 2 uses $\lambda_{\text{sup}} = 1.0$ and $\lambda_{\text{align}} = 0.5$ with frozen teacher representations.

---

<h3 id="citation">Citation</h3>

```bibtex
@mastersthesis{farheen2026knowledge,
  author  = {Farheen, Tasneem Jahan},
  title   = {Knowledge Distillation in Split Learning for Heterogeneous Clinical Tabular Data},
  school  = {BRAC University},
  address = {Dhaka, Bangladesh},
  year    = {2026},
  month   = {March},
  url     = {[https://dspace.bracu.ac.bd/items/fcb0c1f9-183f-4bd4-aba8-3f915c5e4c58](https://dspace.bracu.ac.bd/items/fcb0c1f9-183f-4bd4-aba8-3f915c5e4c58)}
}
