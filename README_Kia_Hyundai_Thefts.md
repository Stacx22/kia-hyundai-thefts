# Kia–Hyundai Thefts: Data Story for Urban Safety Leaders (R)

## Overview
A reproducible **R Markdown** brief that synthesizes multiple public datasets to show where, when, and how strongly **Kia/Hyundai thefts** surged across U.S. cities. Audience: policymakers & law-enforcement analysts. Includes six visuals—**pie, donut, stacked bar, treemap, a Milwaukee monthly area chart, and a multi-city stacked area chart**—and a call to action for targeted deterrence.

## Repo Structure
```
kia-hyundai-thefts/
├─ data/                 # monthly & yearly CSVs
├─ R/                    # wrangling + plotting scripts
├─ reports/              # knitted PDF/HTML; exported figures
├─ renv/                 # optional R env lock (renv)
└─ README.md
```

## Quick Start (R)
```r
install.packages(c("tidyverse","lubridate","janitor","scales","treemap","ggplot2"))
# optional: renv::restore()
rmarkdown::render("R/KiaHyundai_Story.Rmd", output_format = "pdf_document")
```

## Pipeline
1. **Ingest & Clean:** normalize column names, parse dates, fix types, deduplicate  
2. **Transform:** group by city/state/month; compute Kia/Hyundai vs other thefts and percentages  
3. **Visualize:** required six visuals + legends/annotations for policy audiences  
4. **Narrative:** context, key findings, and **call to action** (targeted deterrence & reporting)

## Deliverables
- `reports/KiaHyundai_Story.pdf` (or HTML)  
- `reports/figures/` with all charts for reuse in briefs or slides

## Notes & Ethics
- Data quality varies by municipality; caveats and limitations are documented in the brief.  
- Avoids sensationalism; focuses on comparability, trend clarity, and actionable insights.
