---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* **M.Sc. in Computer Science and Engineering** | BRAC University, Bangladesh *(May 2024 – Mar 2026)*[cite: 1]
  * *Thesis:* Knowledge Distillation in Split Learning for Heterogeneous Clinical Tabular Data[cite: 1]
  * Proposed a privacy-preserving split learning framework for diabetes risk prediction across heterogeneous clinical datasets[cite: 1].
  * Designed and evaluated logit-level and encoder-level distillation strategies under extreme few-shot supervision[cite: 1].
  * Benchmarked MLP, SAINT, and TabM student models, demonstrating consistent gains over scratch training in low-resource settings[cite: 1].
  * *Award:* Secured a 40% merit-based scholarship through undergraduate academic performance[cite: 1].
* **B.Sc. in Computer Science and Engineering** | American International University-Bangladesh *(Sep 2019 – May 2023)*[cite: 1]
  * *Major:* Software Engineering[cite: 1]
  * *Thesis:* Heart Disease Prediction Using Machine Learning[cite: 1]
  * Compared five ML classifiers (KNN, Naïve Bayes, SVM, Logistic Regression, and Random Forest) on merged multi-source clinical datasets[cite: 1].
  * Applied 10-fold cross-validation and hyperparameter tuning, selecting the best-performing model via ROC-AUC analysis[cite: 1].
  * *Honors:* Dean's List, Faculty of Science and Technology (Received for 3 undergraduate semesters)[cite: 1].

Work Experience
======
* **Computer Science Teacher** | Mastermind English Medium School, Dhaka, Bangladesh *(Jan 2024 – Present)*[cite: 1]
  * Develop and deliver lesson plans on MS Word, Python, and AI[cite: 1].
  * Conduct weekly lab sessions, improving hands-on skills by 85% based on assessments[cite: 1].
  * Design and evaluate digital assessments for academic progress tracking[cite: 1].

* **Full Stack Developer** | Upwork Inc. *(Oct 2022 – May 2023)*[cite: 1]
  * Built and maintained a Laravel-based PHP web application with a Vue.js front end for a client engagement, following MVC architecture and object-oriented PHP practices[cite: 1].
  * Optimized code and database queries, improving application performance by 20%[cite: 1].
  * Managed version control with Git and supported deployment processes[cite: 1].

Featured Projects
======
* **Weather API Data Pipeline & Power BI Dashboard**[cite: 1]
  * Built an end-to-end Python ETL pipeline to ingest hourly weather observations from the Open-Meteo API, transform raw API responses, and store structured data for analysis[cite: 1].
  * Performed SQL-based analysis of temperature, humidity, and wind-speed patterns across cities and time periods[cite: 1].
  * Developed an interactive Power BI dashboard with KPI cards, city comparisons, and time-based visualizations to identify weather trends[cite: 1].

* **E-Commerce Customer Retention & Behavioral Segmentation Engine**[cite: 1]
  * Extracted and combined data across transaction, customer, and product tables using multi-table SQL joins and aggregations to build a unified analytical dataset[cite: 1].
  * Contrasted Rule-Based RFM quantile segmentation with ML-driven K-Means clustering, optimizing clusters via log-transformations and the Elbow Method[cite: 1].
  * Evaluated customer segments through a custom multi-metric Fitness Score to surface actionable insights[cite: 1].

Skills
======
* **Programming Languages & Frameworks:** Python, Java, JavaScript, SQL, Vue.js, React, Laravel[cite: 1]
* **Tools & Platforms:** Google Colab, VS Code, Git/GitHub, Microsoft Excel, Power BI[cite: 1]
* **Research Skills:** Academic writing, data analysis, literature review[cite: 1]
* **Soft Skills:** Problem-solving, teamwork, adaptability[cite: 1]

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
