# Tick-Borne Disease Analysis

## Project Overview

This project analyzes the distribution and trends of tick-borne diseases in Georgia. The dataset includes confirmed cases of tick-borne illnesses, patient demographics, test results, and related medical information. The analysis explores disease burden, trends over time, hotspot counties, and other key factors.

## Folder Structure

-   **data/**: Contains raw and cleaned data files.
-   **code/**: Includes all R and Quarto scripts used for data cleaning, analysis, and reporting.
-   **results/**: Stores output files like figures, tables, and reports.
-   **documentation/**: Contains the readme and any other relevant documentation.
-   **assets/**: Contains static assets like manually generated schematics/diagrams, bibtex files, csl style files, PDFs of references, and other such content.

This project uses relative paths, which allows for easier replication of the analysis on different systems. Below is a description of the folder structure:

-   **data/**: Contains raw and cleaned data files. Example file path:
    -   `data/raw/tick_borne_diseases.csv` - Raw dataset for analysis.
    -   `data/cleaned/tick_borne_cleaned.csv` - Cleaned dataset after preprocessing.
-   **code/**: Contains R or Quarto scripts that perform data cleaning, analysis, and generate visualizations. Example file path:
    -   `code/processing-code-tickcases.qmd` - Script to clean the raw data.
    -   `code/analysis-code-tickcases.qmd` - Script to perform bivariate and multivariable analyses.
-   **results/**: Stores output files like figures and tables. Example file path:
    -   `results/figures/disease_histogram.png` - Visualization of disease distribution by disease type.

## Reproducibility Instructions

1.  Clone or download this repository.
2.  Ensure all required R packages are installed: \`\`\`r install.packages(c("readxl", "here" "skimr", "tidyr", "dplyr", "ggplot2", "tidymodels", "kableExtra", "lubridate"))

# 
