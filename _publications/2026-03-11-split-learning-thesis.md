---
title: "Knowledge Distillation in Split Learning for Heterogeneous Clinical Tabular Data"
collection: publications
category: "thesis"
permalink: /publication/2026-03-04-split-learning-thesis
date: 2026-03-11
venue: 'BRAC University Institutional Repository (DSpace)'
tags:
  - Split Learning
  - Knowledge Distillation
  - Tabular Deep Learning
  - PyTorch
---

<div class="pub-citation">
  <strong>Tasneem Jahan Farheen</strong><br>
  <em>Master's Thesis</em> — BRAC University Institutional Repository (DSpace), 2026
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
    <i class="fas fa-file-pdf"></i> Read Full Paper (DSpace)
  </a>
  <a href="/talks/">
    <i class="fas fa-chalkboard-teacher"></i> Defense Slides
  </a>
</div>

---

### Highlights & Key Findings

* **Decentralized Knowledge Transfer:** Combines split learning with logit-level and latent encoder-level knowledge distillation, allowing multi-institution collaboration without sharing raw patient tabular records.
* **Few-Shot Performance Boost:** Under extreme label scarcity, logit-level distillation transfers strong decision boundaries from population teacher models to lightweight target models, significantly lifting discriminative performance (ROC-AUC).
* **Cross-Domain Calibration:** Encoder-level alignment minimizes feature divergence under clinical distribution shift, substantially improving probabilistic calibration (reducing overconfidence).
* **Architecture Benchmark:** Explores both traditional MLPs and modern tabular transformer architectures (**SAINT**, **TabM**).

---

### Abstract

The growing availability of clinical data across institutions creates new opportunities for improved disease risk prediction. However, privacy regulations, institutional policies, and limited labeled data restrict centralized model training, particularly in low-resource settings. To address these challenges, this study presents a privacy-preserving framework that integrates split learning and knowledge distillation for diabetes risk prediction using heterogeneous tabular datasets.

This work systematically evaluates two complementary transfer mechanisms:

1. **Logit-Level Knowledge Distillation:** Transfers predictive decision boundaries from high-capacity teacher models collaboratively trained on large population datasets to lightweight student models in low-resource target domains.
2. **Encoder-Level Knowledge Distillation:** Aligns latent feature representations within a split learning architecture.

Both approaches maintain strict data privacy by keeping raw patient data local and exchanging only intermediate activations. Experimental results under few-shot supervision indicate that logit-level distillation substantially improves discriminative performance, particularly in extremely low-label scenarios while stabilizing training across heterogeneous domains. Encoder-level distillation further improves probabilistic calibration and representation alignment under cross-domain distribution shifts.

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
