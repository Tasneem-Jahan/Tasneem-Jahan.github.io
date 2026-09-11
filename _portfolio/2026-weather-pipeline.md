---
title: "Weather API Data Pipeline & Power BI Dashboard"
excerpt: "An automated Python ETL pipeline ingesting Open-Meteo observations with SQL relational modeling, longitudinal analytics, and an interactive Power BI dashboard."
collection: portfolio
permalink: /portfolio/2026-weather-pipeline/
date: 2026-08-07
---

<div class="pub-citation">
  <strong>Tasneem Jahan Farheen</strong><br>
  <em>Automated Data Engineering, Relational Modeling & BI Analytics</em> — August 2026
</div>

<div class="research-tags">
  <span class="research-tag">Python</span>
  <span class="research-tag">Open-Meteo API</span>
  <span class="research-tag">PostgreSQL / SQL</span>
  <span class="research-tag">ETL Engineering</span>
  <span class="research-tag">Power BI</span>
  <span class="research-tag">Data Modeling</span>
</div>

<div class="pub-actions">
  <a href="https://github.com/Tasneem-Jahan/weather-api-data-pipeline" target="_blank" rel="noopener">
    <i class="fab fa-github"></i> View GitHub Repository
  </a>
  <a href="#pipeline-workflow">
    <i class="fas fa-project-diagram"></i> Architecture
  </a>
  <a href="#dashboard-analytics">
    <i class="fas fa-chart-line"></i> Dashboard & Insights
  </a>
</div>

---

### Project Overview

This project implements an end-to-end automated data engineering pipeline designed to ingest, validate and structure high-frequency meteorological time-series records from the **Open-Meteo REST API**. The pipeline automates data extraction, standardizes nested JSON responses, persists relational schemas into a SQL database and powers an interactive **Power BI** dashboard for climate monitoring, diurnal tracking and comparative cross-city analytics.

<div style="display: flex; flex-direction: row; align-items: center; justify-content: space-between; gap: 8px; margin: 24px 0; padding: 16px; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 10px; width: 100%; box-sizing: border-box; overflow-x: auto;">
  
  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-cloud-sun"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Open-Meteo API</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Hourly Observation Endpoints</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fab fa-python"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Python ETL Worker</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Validation, Cleaning & Parsing</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-database"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Relational DB</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">SQL Star Schema Modeling</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-chart-line"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Power BI</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">KPI Dashboards & Trend DAX</div>
  </div>

</div>

---

<h3 id="pipeline-workflow">Technical Highlights & Pipeline Design</h3>

* **Automated Data Ingestion (API Extraction):**
  * Automated periodic polling of the Open-Meteo REST API across multi-city coordinate clusters (London, New York, Tokyo).
  * Built defensive API request wrappers with connection timeout handling, exponential backoff retries and HTTP response code validation.
* **Data Transformation & Integrity (ETL Processing):**
  * Extracted and flattened nested JSON responses into clean pandas DataFrames.
  * Standardized measurement units (Celsius, percentage relative humidity, km/h wind velocity) and parsed ISO 8601 timestamps into aligned UTC/local datetime dimensions.
  * Enforced schema validation to drop null sensor records and prevent duplicate entry insertion.
* **Relational Schema Design & Data Modeling (SQL):**
  * Modeled an analytical **Star Schema** separating Dimension entities (`Dim_City`, `Dim_Date`, `Dim_Condition`) from an aggregated Fact table (`Fact_Weather_Observations`).
  * Enforced primary and foreign key integrity constraints, indexation on timestamp lookups and idempotent upserts to ensure consistent runs.
  * Formulated SQL aggregation scripts computing rolling 7-day temperature means, diurnal temperature spreads, and humidity variance.
* **Business Intelligence & Reporting (Power BI & DAX):**
  * Established direct connectivity to the relational data store with scheduled refreshes.
  * Formulated calculated measures in **DAX** to surface summary statistics, extreme anomaly alerts and dynamic city-level benchmark cards.

---

<h3 id="dashboard-analytics">Interactive Reporting Suite & Analytical Insights</h3>

<div style="background: #ffffff; border: 1px solid var(--surface-border, #e2e8f0); border-radius: 10px; padding: 1.25rem; margin: 1.5rem 0; box-shadow: 0 2px 8px rgba(0,0,0,0.04); text-align: center;">
  
  <a href="/images/weather-analytics-dashboard.png" download="Weather-Analytics-Dashboard.png" title="Click to download full-resolution image">
    <img src="/images/weather-analytics-dashboard.png" alt="Power BI Weather Analytics Dashboard" style="width: 100%; border-radius: 6px; border: 1px solid #e2e8f0; margin-bottom: 0.75rem; cursor: pointer; transition: opacity 0.2s ease;" onmouseover="this.style.opacity='0.95'" onmouseout="this.style.opacity='1'">
  </a>

  <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 0.5rem; margin-top: 0.5rem;">
    <p style="font-size: 0.85rem; color: #64748b; margin: 0; text-align: left;">
      <em>Figure 1: Power BI interactive reporting suite monitoring real-time meteorological observations across London, New York, and Tokyo.</em>
    </p>    
  </div>

</div>

| Dimension | Analytical Findings | Clinical / Operational Implication |
| :--- | :--- | :--- |
| **Thermal Range** | Spans 12.70°C to 35.70°C across observed regions | Critical for assessing localized urban heat-island intensity |
| **City Distribution** | Tokyo leads in mean heat; London maintains cooler baselines | Informs localized environmental and HVAC operational models |
| **Moisture Profiles** | Tokyo displays sustained high humidity (>80%); London remains moderate | Directly affects heat-index calculations and weather forecasting |
| **Wind Dynamics** | London leads with peak gusts of 23.40 km/h; Tokyo averages ~4 km/h | Validates localized wind variance patterns and structural exposure |

---

### Tech Stack

| Layer | Tools | Responsibility |
| :--- | :--- | :--- |
| **Extraction** | Python (`requests`), Open-Meteo REST API | Automated API polling, payload ingestion, rate limit mitigation |
| **Processing** | Python (`pandas`, `numpy`) | Data cleaning, type conversion, JSON flattening, UTC alignment |
| **Storage** | PostgreSQL / SQL, SQLAlchemy | Dimensional modeling (Star Schema), relational constraints, aggregations |
| **Analytics & UI** | Power BI, DAX | Metric engineering, time-series visualization, slicer controls |
