# 🧬 Gene Biotype Annotation with biomaRt

This repository contains an R script to annotate a gene list (human or mouse) with gene biotypes using the Ensembl BioMart service via the `biomaRt` package.

## 📌 Purpose

Given a list of gene symbols (e.g., from RNA-seq or microarray data), this pipeline fetches corresponding **gene biotypes** (e.g., `protein_coding`, `lncRNA`, `pseudogene`, etc.) from Ensembl and exports the annotated list to Excel.



## 🚀 Getting Started

### Requirements

- R ≥ 4.1.0
- Internet connection (for BioMart queries)
- Packages:
  - `biomaRt`
  - `readxl`
  - `writexl`
  - `dplyr`

### 📥 Installation

Open R or RStudio and run:

```r
if (!requireNamespace("BiocManager", quietly = TRUE))
  install.packages("BiocManager")
# For mouse
# mart <- useEnsembl(biomart = "genes", dataset = "mmusculus_gene_ensembl")

# For human
mart <- useEnsembl(biomart = "genes", dataset = "hsapiens_gene_ensembl")

BiocManager::install(c("biomaRt", "readxl", "writexl"))

