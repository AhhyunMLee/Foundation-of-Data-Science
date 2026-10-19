# QBS 103 Final Project

Analysis of maternal blood gene expression in relation to vitamin D, preeclampsia,
and gestational age, using data from GEO accession
[GSE85307](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE85307)
([original paper](https://pubmed.ncbi.nlm.nih.gov/27841759/)).

## Data

- 157 pregnant women
- Gene expression for 500 probes (Affymetrix Human Gene 1.0 ST Array)
- Covariates: maternal age, BMI, vitamin D, asthma, pregnancy outcome
  (preeclampsia vs normal), gestational age at blood draw and at delivery,
  and microarray batch

## Variables of Interest

| Role | Variable |
|---|---|
| Gene | CXCR2 |
| Continuous covariate | Maternal vitamin D at baseline (ng/mL) |
| Categorical covariate 1 | Pregnancy outcome (Normal vs Preeclampsia) |
| Categorical covariate 2 | Trimester of blood draw (1st: <14 weeks, 2nd: >=14 weeks), derived from gestational age at blood draw |

## Repository Contents

| File | Description |
|---|---|
| `Submission1.Rmd` | Data wrangling and plots for Submission 1 (histogram, scatterplot, boxplot) |
| `Submission1.pdf` | Knitted output of `Submission1.Rmd` |
| `data/GSE85307_geneExpression.csv` | Gene expression data (rows = probe IDs, columns = samples) |
| `data/GSE85307_covar.csv` | Covariate data for each sample |
| `data/GSE85307_geneNames.csv` | Linker file between probe IDs and gene names |

## How to Run

1. Clone this repository (or download it as a ZIP file).
2. Open `Submission1.Rmd` in RStudio from the repository folder.
3. Click **Knit**. The data files are read from the `data/` folder, so keep the folder
   structure as is.

Required R package: `ggplot2` (plus `rmarkdown` and a LaTeX installation to knit to PDF).
