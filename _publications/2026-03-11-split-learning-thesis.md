---
title: "Knowledge Distillation in Split Learning for Heterogeneous Clinical Tabular Data"
collection: publications
category: manuscripts
permalink: /publication/2026-03-04-split-learning-thesis
excerpt: "Master's Thesis exploring logit-level and encoder-level knowledge distillation in split learning architectures for clinical tabular datasets."
date: 2026-03-04
venue: "BRAC University Institutional Repository (DSpace)"
paperurl: "https://dspace.bracu.ac.bd/items/fcb0c1f9-183f-4bd4-aba8-3f915c5e4c58"
citation: 'Tasneem Jahan Farheen. (2026). "Knowledge Distillation in Split Learning for Heterogeneous Clinical Tabular Data." M.Sc. Thesis, Department of Computer Science and Engineering, BRAC University.'
---

### Abstract
The growing availability of clinical data across institutions creates new opportunities for improved disease risk prediction. However, privacy regulations, institutional policies, and limited labeled data restrict centralized model training, particularly in low-resource settings. To address these challenges, this study presents a privacypreserving framework that integrates split learning and knowledge distillation for diabetes risk prediction using heterogeneous tabular datasets. This work systematically evaluates two complementary transfer mechanisms. The first approach utilizes logit-level knowledge distillation to transfer predictive decision boundaries from high-capacity teacher models, collaboratively trained on large population datasets, to lightweight student models in low-resource target domains. The second approach implements encoder-level distillation to align latent feature representations within a split learning architecture. Both approaches maintain strict data privacy by keeping raw patient data local and exchanging only intermediate activations. Experimental results under few-shot supervision indicate that logit-level distillation substantially improves discriminative performance, particularly in extremely low-label scenarios while stabilizing training across heterogeneous domains. Encoder-level distillation further improves probabilistic calibration and representation alignment under crossdomain distribution shifts. These findings underscore the significance of structured knowledge transfer in privacy-preserving clinical machine learning and offer practical recommendations for deploying reliable models in heterogeneous healthcare environments.

* **Repository / Download**: [BRACU DSpace Link](https://dspace.bracu.ac.bd/items/fcb0c1f9-183f-4bd4-aba8-3f915c5e4c58)
