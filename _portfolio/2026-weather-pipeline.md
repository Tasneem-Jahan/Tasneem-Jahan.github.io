---
title: "Weather API Data Pipeline & Power BI Dashboard"
excerpt: "An automated Python ETL pipeline ingesting Open-Meteo observations with SQL trend analysis and an interactive Power BI dashboard."
collection: portfolio
permalink: /portfolio/2026-weather-pipeline/
date: 2026-08-03
---

<div class="pub-citation">
  <strong>Tasneem Jahan Farheen</strong><br>
  <em>Automated ETL Pipeline, Relational Modeling & BI Analytics</em> — August 2026
</div>

<div class="research-tags">
  <span class="research-tag">Python</span>
  <span class="research-tag">Open-Meteo API</span>
  <span class="research-tag">SQL</span>
  <span class="research-tag">ETL Engineering</span>
  <span class="research-tag">Power BI</span>
  <span class="research-tag">Data Modeling</span>
</div>

<div class="pub-actions">
  <a href="https://github.com/Tasneem-Jahan/weather-api-data-pipeline" target="_blank" rel="noopener">
    <i class="fab fa-github"></i> View GitHub Repository
  </a>
</div>

---

### Project Overview

Engineered an automated, end-to-end Python ETL data pipeline designed to ingest, normalize, and store continuous meteorological data from the **Open-Meteo REST API**. The pipeline automates data extraction, applies validation and schema enforcement, persists records into a structured SQL database, and powers an interactive **Power BI** dashboard for climate monitoring and exploratory trend analysis.

<div class="pipeline-diagram">
  <div class="step-card">
    <div class="step-icon"><i class="fas fa-cloud-sun"></i></div>
    <div class="step-title">Open-Meteo API</div>
    <div class="step-sub">JSON Endpoints</div>
  </div>
  
  <div class="step-arrow"><i class="fas fa-arrow-right"></i></div>

  <div class="step-card">
    <div class="step-icon"><i class="fab fa-python"></i></div>
    <div class="step-title">Python ETL Worker</div>
    <div class="step-sub">Validation & Clean</div>
  </div>

  <div class="step-arrow"><i class="fas fa-arrow-right"></i></div>

  <div class="step-card">
    <div class="step-icon"><i class="fas fa-database"></i></div>
    <div class="step-title">Relational DB</div>
    <div class="step-sub">SQL Star Schema</div>
  </div>

  <div class="step-arrow"><i class="fas fa-arrow-right"></i></div>

  <div class="step-card">
    <div class="step-icon"><i class="fas fa-chart-line"></i></div>
    <div class="step-title">Power BI</div>
    <div class="step-sub">KPIs & Trends</div>
  </div>
</div>
