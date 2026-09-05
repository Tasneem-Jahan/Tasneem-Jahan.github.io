---
permalink: /
title: "About Me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a Master's graduate in Computer Science and Engineering from BRAC University, specializing in machine learning for healthcare informatics.

> **Prospective PhD Student:** I am actively seeking PhD opportunities in Machine Learning and Healthcare Informatics starting **Fall 2027**.

In my M.Sc. thesis, I investigated split learning frameworks for heterogeneous clinical tabular data, evaluating logit-level and encoder-level knowledge distillation under few-shot supervision with MLP, SAINT, and TabM architectures. My B.Sc. thesis evaluated machine learning classifiers for heart disease risk prediction across multi-source clinical datasets using rigorous cross-validation, hyperparameter tuning, and ROC-AUC metrics.

*I also bring a working foundation in full-stack software development and data engineering.*

[Download CV]({{ site.url }}{{ site.baseurl }}/files/CV_Tasneem_Jahan_Farheen.pdf){: .btn .btn--primary}
[Email Me](mailto:tasneem_jahan@outlook.com){: .btn .btn--info}

---

### Research Interests

* **Agentic AI & Multimodal Clinical Decision Support**: Developing multi-agent retrieval-augmented generation (RAG) frameworks integrating electronic health records (EHR), medical imaging, and clinical notes.
* **Uncertainty Quantification & Model Calibration**: Designing reliable uncertainty estimation methods so clinical agents flag limitations rather than making overconfident predictions in high-stakes environments.
* **Algorithmic Fairness & Bias Mitigation**: Mitigating non-clinical proxy variable exploitation (e.g., insurance status, socioeconomic factors) to reduce disparities in healthcare ML.
* **Decentralized & Privacy-Preserving Learning**: Split learning, federated learning, and knowledge distillation for distributed medical systems.

---

### Education

* **M.Sc. in Computer Science and Engineering** | BRAC University *(2024 – 2026)*
  * *Thesis:* Knowledge Distillation in Split Learning for Heterogeneous Clinical Tabular Data
  * *Honors:* 40% Merit-Based Academic Scholarship

* **B.Sc. in Computer Science and Engineering** | American International University-Bangladesh (AIUB) *(2019 – 2023)*
  * *Major:* Software Engineering
  * *Thesis:* Heart Disease Prediction Using Machine Learning
  * *Honors:* Dean's List (3 Semesters)

---

### Featured Research

---
layout: archive
title: "Portfolio"
permalink: /portfolio/
author_profile: true
---

{% include base_path %}


{% for post in site.portfolio %}
  {% include archive-single.html %}
{% endfor %}



* **Knowledge Distillation in Split Learning for Heterogeneous Clinical Tabular Data**  
  Proposed a split learning framework for diabetes risk prediction across heterogeneous clinical tabular datasets. Designed and evaluated logit-level and encoder-level distillation strategies under extreme few-shot supervision, benchmarking MLP, SAINT, and TabM student models.  
  [[Thesis PDF]](https://dspace.bracu.ac.bd/items/fcb0c1f9-183f-4bd4-aba8-3f915c5e4c58)

* **Heart Disease Prediction Using Machine Learning**  
  Conducted a comparative study of five machine learning classifiers (KNN, Naïve Bayes, SVM, Logistic Regression, Random Forest) on integrated multi-source clinical datasets using 10-fold cross-validation and ROC-AUC analysis.

For full-stack and applied data engineering work, see my [Projects]({{ site.url }}{{ site.baseurl }}/portfolio/) page.
