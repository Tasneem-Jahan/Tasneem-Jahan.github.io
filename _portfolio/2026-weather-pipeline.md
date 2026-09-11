---
title: "Weather API Data Pipeline & Power BI Dashboard"
excerpt: "An automated Python ETL pipeline ingesting Open-Meteo observations with SQL trend analysis and an interactive Power BI dashboard."
collection: portfolio
permalink: /portfolio/2026-weather-pipeline/
date: 2026-08-07
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

<div style="display: flex; flex-direction: row; align-items: center; justify-content: space-between; gap: 8px; margin: 24px 0; padding: 16px; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 10px; width: 100%; box-sizing: border-box; overflow-x: auto;">
  
  <!-- Step 1 -->
  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-cloud-sun"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Open-Meteo API</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">JSON Endpoints</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <!-- Step 2 -->
  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fab fa-python"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Python Worker</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">Validation & Clean</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <!-- Step 3 -->
  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-database"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Relational DB</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">SQL Star Schema</div>
  </div>

  <div style="color: #94a3b8; font-size: 0.9rem; flex-shrink: 0;"><i class="fas fa-arrow-right"></i></div>

  <!-- Step 4 -->
  <div style="flex: 1; min-width: 110px; text-align: center; padding: 12px 6px; background: #ffffff; border: 1px solid #e2e8f0; border-radius: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.04);">
    <div style="font-size: 1.4rem; color: #0f766e; margin-bottom: 4px;"><i class="fas fa-chart-line"></i></div>
    <div style="font-weight: 700; font-size: 0.82rem; color: #1e293b; line-height: 1.2;">Power BI</div>
    <div style="font-size: 0.72rem; color: #64748b; margin-top: 3px;">KPIs & Trends</div>
  </div>

</div>
<div style="background: #ffffff; border: 1px solid var(--surface-border, #e2e8f0); border-radius: 10px; padding: 1.25rem; margin: 1.5rem 0; box-shadow: 0 2px 8px rgba(0,0,0,0.04); text-align: center;">
  
  <!-- Clickable Image for Download -->
  <a href="/images/weather-analytics-dashboard.png" download="Weather-Analytics-Dashboard.png" title="Click to download full-resolution image">
    <img src="/images/weather-analytics-dashboard.png" alt="Power BI Weather Analytics Dashboard" style="width: 100%; border-radius: 6px; border: 1px solid #e2e8f0; margin-bottom: 0.75rem; cursor: pointer; transition: opacity 0.2s ease;" onmouseover="this.style.opacity='0.95'" onmouseout="this.style.opacity='1'">
  </a>

  <!-- Caption & Direct Download Button -->
  <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 0.5rem; margin-top: 0.5rem;">
    <p style="font-size: 0.85rem; color: #64748b; margin: 0; text-align: left;">
      <em>Figure 1: Power BI interactive reporting suite monitoring real-time meteorological observations across London, New York and Tokyo.</em>
    </p>
  </div>

</div>
