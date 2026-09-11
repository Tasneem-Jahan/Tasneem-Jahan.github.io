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
  <a href="#manual-citation">
    <i class="fas fa-quote-right"></i> Cite (BibTeX)
  </a>
</div>

---

### Core Research Contributions

* **Privacy-Preserving Cross-Silo Collaboration:** Introduces a decentralized framework that decouples tabular feature encoders from a shared server backbone, ensuring patient-level tabular records never leave institutional boundaries while transmitting only intermediate representations (smash data)[cite: 1].
* **Dual Knowledge Distillation Paradigms:** Systematically formulates and contrasts two transfer pathways from a collaborative FT-Transformer teacher: **Logit-Level KD** (soft predictive decision boundaries) and **Encoder-Level KD** (latent latent-space alignment via MSE)[cite: 1].
* **Extreme Few-Shot Robustness ($K \in \{5, 10, 20\}$):** Demonstrates that teacher guidance offsets severe sample scarcity, improving discriminative power up to $+16.09\%$ in ROC-AUC for capacity-constrained architectures at $K=5$[cite: 1].
* **Decoupled Discrimination vs. Calibration Dynamics:** Uncovers that logit-level transfer primarily optimizes decision ranking (ROC-AUC), whereas encoder-level alignment drives model reliability by substantially reducing Expected Calibration Error and Brier scores under cross-domain distribution shifts[cite: 1].
* **Multi-Cohort Heterogeneous Validation:** Validated across distinct feature modalities—bridging continuous laboratory measurements (NHANES, HRS, Pima) and pure symptom-based binary clinical profiles (Sylhet 520-cohort)[cite: 1].

---

### Abstract

The growing availability of clinical data across institutions creates new opportunities for improved disease risk prediction[cite: 1]. However, privacy regulations, institutional policies, and limited labeled data restrict centralized model training, particularly in low-resource settings[cite: 1]. To address these challenges, this study presents a privacy-preserving framework that integrates split learning and knowledge distillation for diabetes risk prediction using heterogeneous tabular datasets[cite: 1]. 

This work systematically evaluates two complementary transfer mechanisms[cite: 1]:
1. **Logit-Level Knowledge Distillation:** Transfers predictive decision boundaries from high-capacity teacher models, collaboratively trained on large population datasets (NHANES and HRS), to lightweight student models in low-resource target domains[cite: 1].
2. **Encoder-Level Knowledge Distillation:** Aligns latent feature representations within a split learning architecture using mean squared error feature matching[cite: 1].

Both approaches maintain strict data privacy by keeping raw patient data local and exchanging only intermediate activations[cite: 1]. Experimental results under few-shot supervision indicate that logit-level distillation substantially improves discriminative performance, particularly in extremely low-label scenarios, while stabilizing training across heterogeneous domains[cite: 1]. Encoder-level distillation further improves probabilistic calibration and representation alignment under cross-domain distribution shifts[cite: 1]. These findings underscore the significance of structured knowledge transfer in privacy-preserving clinical machine learning and offer practical recommendations for deploying reliable models in heterogeneous healthcare environments[cite: 1].

---

<div id="manual-citation">
  <h3>Citation</h3>
  <p style="font-size: 0.95rem; color: #334155; margin-bottom: 0.8rem;">
    <strong>APA:</strong><br>
    Farheen, T. J. (2026). <em>Knowledge Distillation in Split Learning for Heterogeneous Clinical Tabular Data</em> (Master's thesis, BRAC University). BRAC University Institutional Repository.
  </p>

  <p style="font-size: 0.95rem; color: #334155; margin-bottom: 0.5rem;">
    <strong>BibTeX:</strong>
  </p>
  <pre style="background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 8px; padding: 1rem; font-size: 0.85rem; line-height: 1.5; overflow-x: auto; color: #1e293b;"><code>@mastersthesis{farheen2026knowledge,
  author  = {Farheen, Tasneem Jahan},
  title   = {Knowledge Distillation in Split Learning for Heterogeneous Clinical Tabular Data},
  school  = {BRAC University},
  address = {Dhaka, Bangladesh},
  year    = {2026},
  month   = {March},
  url     = {https://dspace.bracu.ac.bd/items/fcb0c1f9-183f-4bd4-aba8-3f915c5e4c58}
}</code></pre>
</div>
