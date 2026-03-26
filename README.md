# IPMC Electrode Material Performance Meta-Analysis

**Author:** Krish Chopra  
**Course:** AP Research  
**Paper:** An Empirical Analysis of IPMC Electrode Materials in a Robotics Application

---

## Overview

This repository contains the R Notebook used to conduct a meta-analysis examining how electrode material affects the actuation performance and durability of Ionic Polymer-Metal Composites (IPMCs) in load-bearing robotics applications. The analysis synthesizes data from 20 peer-reviewed studies published between 2000 and 2025, evaluating five electrode materials across four performance metrics.

---

## Research Question

Do CNT-based electrodes demonstrate greater actuation displacement and longer durability under repeated load-bearing cycles compared to silver or copper electrodes?

---

## Repository Structure

```
├── IPMC_Meta_Analysis.Rmd        # Main R Notebook (all analysis)
├── MasterSheet.csv               # Combined study data
├── MetaData.csv                  # Study metadata (authors, year, DOI)
├── PerformanceMetrics.csv        # Response time, strain data
├── FabricationSpecifications.csv # Electrode fabrication details
├── TestingConditions.csv         # Environmental and testing parameters
└── results/
    ├── results_summary_by_electrode.csv      # Descriptive stats with 95% CIs
    ├── results_meta_analysis_coefficients.csv # Model coefficients
    ├── results_heterogeneity_quality.csv      # I², τ², Q statistics
    ├── results_pairwise_comparisons.csv       # All pairwise t-test results
    └── results_study_level_data.csv           # Study-level data with effect sizes
```

---

## Analysis Pipeline

The notebook follows a structured 12-step pipeline:

1. **Package Loading** — metafor, dplyr, ggplot2, kableExtra, gridExtra
2. **Data Import** — reads and summarizes all five CSV input files
3. **Data Preprocessing** — factor encoding, log transformation of cycle counts, strain calculation
4. **Descriptive Statistics** — mean ± SD for all metrics grouped by electrode material
5. **Effect Size Calculation** — Hedge's g computed relative to gold electrode baseline
6. **Meta-Analysis** — random-effects models (REML) for displacement, force, resistance, and durability using the `metafor` package
7. **Heterogeneity Assessment** — I², τ², and Q statistics for all models
8. **Pairwise Comparisons** — t-tests across all electrode pairs with -log₁₀(p) visualization
9. **Hypothesis Testing** — direct CNT vs. silver and copper comparison across all metrics
10. **Export** — results written to CSV files
11. **Key Findings Summary** — automated performance rankings and hypothesis verdict
12. **Conclusions** — statistical findings and practical implications

---

## Key Results

| Electrode | Displacement (mm) | Cycles to Failure | Force (mN) |
|---|---|---|---|
| CNT Composite | 17.43 ± 2.66 | 8,400 ± 594 | 14.18 ± 2.69 |
| Gold (Au) | 16.45 ± 12.89 | 6,150 ± 1,399 | 14.75 ± 3.39 |
| Platinum (Pt) | 8.57 ± 0.75 | 5,675 ± 359 | 12.10 ± 0.98 |
| Silver (Ag) | 9.55 ± 3.55 | 4,260 ± 230 | 6.98 ± 2.72 |
| Copper (Cu) | 10.83 ± 0.85 | 3,950 ± 150 | 9.83 ± 0.35 |

**Hypothesis verdict: ✓ SUPPORTED** — CNT electrodes outperform silver and copper in both displacement and durability across all pairwise comparisons.

---

## How to Run

### Requirements

- R version 4.0 or higher
- RStudio (recommended)

### Required Packages

```r
install.packages(c("metafor", "dplyr", "ggplot2", "tidyr", 
                   "knitr", "kableExtra", "scales", "gridExtra"))
```

### Steps

1. Clone the repository
```bash
git clone https://github.com/kool-krish101/AP-Research-IPMC-Testing
```

2. Place all CSV data files in the same directory as the `.Rmd` file

3. Open `IPMC_Meta_Analysis.Rmd` in RStudio

4. Click **Knit** to render the full HTML report, or run chunks individually

---

## Statistical Methods

- **Meta-analysis model:** Random-effects (REML) via `metafor::rma()`
- **Effect sizes:** Hedge's g, computed relative to gold electrode baseline
- **Heterogeneity:** I², τ², and Q statistics — all models showed substantial heterogeneity (I² > 96%)
- **Pairwise comparisons:** Welch two-sample t-tests across all electrode pairs
- **Durability modeling:** Log-transformed cycle counts to normalize right-skewed distributions
- **Moderators:** Environment (aqueous vs. air) and testing frequency (Hz)

---

## Data Sources

All data was extracted from 20 peer-reviewed studies published between 2000–2025, sourced from IEEE Xplore, Web of Science, Scopus, and Google Scholar. Graphical data was digitized using WebPlotDigitizer v4.5. Full citations are available in the paper bibliography.

---

## Contact

For questions about replication or methodology, contact Krish Chopra.
