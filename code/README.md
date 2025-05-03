---
editor_options: 
  markdown: 
    wrap: 300
---

# code

# Folder Structure

[**code/ Contains all scripts used for analysis.**]{.underline}

**- processing-code-tickcases.qmd**\
Script for cleaning and processing raw tick-borne disease case data

**- statistical-analysis.qmd**\
General statistical analysis script

**- statistical-analysis-poverty-rate.qmd**\
Analysis of delay by county-level poverty rate

[**data/ Contains all data files used in the project.**]{.underline}

**- raw-data/**\
Original Excel and CSV files from the Georgia Department of Public Health (GA-DPH)

**- cleaned-data/**\
Cleaned and processed datasets used in analysis

[**results/ Output directory for all generated results.**]{.underline}

**- figures/**\
Saved plots and visualizations for manuscript

\- tables/\
Summary tables for manuscript or reports

\- supplemental-figures/\
Additional exploratory data analysis figures

[**manuscript.qmd Main Quarto document containing the written report.**]{.underline}

[**supplemental-figures.zip Archived bundle of exploratory visuals not included in the main report.**]{.underline}

[**README.txt This file. Describes the folder contents and file purpose.**]{.underline}

# Script Descriptions and Execution Order:

1.  `processing-code-tickcases.qmd`
    -   Loads and cleans raw case data from GA-DPH (Excel format)
    -   Filters for confirmed, positive cases
    -   Identifies inconsistencies in timelines and removes invalid entries
    -   Saves cleaned dataset to `/data/cleaned-data/`
2.  `statistical-analysis.qmd`
    -   Loads cleaned case data
    -   Performs summary statistics and exploratory plots (age, county, disease type, data completeness)
    -   Computes total case duration and flags cases with \>30-day delays
    -   Fits classification models (logistic regression, decision tree, random forest)
    -   Saves figures and tables to `/results/`
3.  `statistical-analysis-poverty-rate.qmd`
    -   Loads county-level poverty data
    -   Merges with delay outcome data by county
    -   Evaluates predictive value of poverty rate using linear and random forest regression
    -   Saves results to `/results/`
4.  `manuscript.qmd`
    -   Compiles findings into a research report for review and submission
    -   Includes inline figures and summary outputs from above scripts

## Execution Notes:

-   Scripts should be run in the above order unless working with cleaned data directly.
-   All `.qmd` files assume required packages are pre-installed (tidyverse, tidymodels, skimr, readxl, etc.).
-   All outputs are written to clearly labeled subfolders within `/results/`.

## Recommendations:

-   Keep all raw data in `/data/raw-data/` and avoid modifying it directly.
-   Re-run the cleaning script if raw data changes.
-   Use version control to track edits to both code and manuscript files.
-   If additional modeling or geographic data is added, consider creating new scripts (e.g. `statistical-analysis-environmental.qmd`).

## Contact:

For questions or issues, contact Hope Grismer at [[hope.grismer\@uga.edu](mailto:hope.grismer@uga.edu){.email}].
