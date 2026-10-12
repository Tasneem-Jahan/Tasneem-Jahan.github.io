---
title: "Confidence-weighted encoder-level knowledge distillation over split learning for few-shot cross-age autism screening"
collection: publications
category: "manuscripts"
permalink: /publications/2026-10-02-autism-screening
date: 2026-10-02
venue: 'Big Data Research (Elsevier), under review'
---

<div class="pub-citation">
  <strong>Tasneem Jahan Farheen</strong>, Nirjhar Gope, Md. Golam Rabiul Alam, Amal Alazba, Ahmed Zohier Elhendi, Mohammad Mehedi Hassan<br>
  <em>Manuscript under review</em> — Big Data Research (Elsevier), 2026
</div>

---

### Highlights & Key Findings

* **Split learning across age groups:** An FT-Transformer teacher is trained on the Adult and Child screening datasets, with a separate client-side encoder for each dataset and a shared server-side encoder. Only activations and gradients cross the institutional boundary.
* **Platt-calibrated logit-level distillation (Framework 1):** At K=5 it helps feedforward students most. The MLP reached ROC-AUC 0.98 ± 0.02 and F1-score 0.95 ± 0.05, and its Brier score fell from 0.12 to 0.05.
* **Confidence-weighted encoder-level distillation (Framework 2):** The student's representations are aligned with the teacher's using a cosine distance weighted by teacher confidence. With 5 labeled samples per class, the Brier score of the best student (TabM) fell from 0.10 ± 0.06 to 0.05 ± 0.04, with a ROC-AUC of 0.99 ± 0.01.
* **Calibration is the clearest gain:** Encoder-level distillation lowered the Brier score in seven of nine model-by-shot comparisons. Framework 2 also scaled better as the label budget grew to K=10 and K=20.
* **Setup:** The Adolescent dataset is the target, with balanced K-shot training at K=5, 10 and 20 per class, three seeds, and MLP, TabM and SAINT-style students. Score-derived features were removed, and all preprocessing was fitted on training data only.
* **Limits:** The Adolescent test set has 16 samples, and the AQ-10 label is computed from the questionnaire items, so absolute scores sit near ceiling. The comparison between transfer methods is the result, not the absolute numbers.

---

### Abstract

Autism screening datasets often differ across age groups, making it challenging for machine learning models trained on one population to generalize to another, and privacy rules prevent institutions from pooling records to close this gap. To address this problem, this study proposes a few-shot split-learning knowledge distillation framework for cross-domain autism screening classification, using the AQ-style Adult and Child datasets as source datasets and the Adolescent dataset as the target dataset. To prevent information leakage, score-derived and domain-proxy features were removed, and all preprocessing steps were fitted only on the training split.

A split-learning teacher model (FT-Transformer) was trained on the source datasets with a separate client-side encoder for each dataset and a shared server-side encoder, so that only activations and gradients crossed the institutional boundary. The pretrained teacher was then adapted to the target domain using balanced K-shot training with K = 5, 10 and 20 labeled samples per class. The study investigated two knowledge distillation approaches, Platt-Calibrated Logit-Level Distillation and Confidence-Weighted Encoder-Level Representation Distillation, evaluating three student models (MLP, TabM and SAINT-style) over three independent random seeds.

The findings show that knowledge distillation improves few-shot classification performance on the target domain. Under severe label scarcity (K = 5), Framework 1 provides strong probability calibration and sensitivity on feedforward architectures (MLP reaching ROC-AUC 0.98 ± 0.02 and F1-score 0.95 ± 0.05), while Framework 2 demonstrates superior architectural robustness and multi-shot scaling across complex students at K = 10 and 20. With just 5 labeled samples per class, Framework 2 cut the Brier score of the best student (TabM) from 0.10 ± 0.06 (trained from scratch) to 0.05 ± 0.04, while reaching a ROC-AUC of 0.99 ± 0.01.
