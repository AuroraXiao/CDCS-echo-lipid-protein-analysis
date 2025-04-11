# CDCS Echocardiography, Lipid and Protein Analysis

This repository contains the full R analysis pipeline for the **MDG5241 Midterm Project**, which investigates the correlation between echocardiographic measurements and plasma molecular profiles (lipids and proteins) from the **Cardiovascular Disease Cohort Study (CDCS)**.

## 📊 Project Overview

The project consists of four key components:

1. **Data Cleaning & Management**
2. **Correlation Heatmap Analysis**
3. **PCA and Clinical Outcome Visualization**
4. **Linear Regression and Multiple Testing**


## 🗂️ Directory Structure

├── data/ # Raw and imputed input datasets 
│ ├── Echoparam_Protein_Lipids_combined_CDCS.txt 
│ ├── clinical data (N=308).txt 
│ └── Echoparam_Protein_Lipids_combined_CDCS_imputed.txt 
├── CDCS-echo-lipid-protein-analysis.Rmd
├── README.md


## 🔧 How to Run the Analysis

> Make sure R (≥ 4.0) and the required packages are installed.

### Step 1: Install Dependencies

```r
install.packages(c("tidyverse", "ggplot2", "dplyr", "readr"))
install.packages("BiocManager")
BiocManager::install("ComplexHeatmap")
BiocManager::install("circlize")

### Step 2: Run Full Pipeline

You can render the RMarkdown file to generate the complete HTML report.

✅ Option 1: In RStudio
Open the RMarkdown file and click "Knit" (recommended).

🧪 Option 2: From R Console
```r
rmarkdown::render("../CDCS-echo-lipid-protein-analysis.Rmd")

💻 Option 3: From Command Line
```bash
Rscript -e "rmarkdown::render('../CDCS-echo-lipid-protein-analysis.Rmd')"

Output: report/MDG5241_midterm_project.html
