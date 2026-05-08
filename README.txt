# Sex-associated mutational differences in cutaneous melanoma

Bioinformatic analysis of sex-associated mutational differences in cutaneous melanoma using TCGA-SKCM and cBioPortal cohorts.

---

# Overview

This repository contains the a bioinformatic pipeline developed for the analysis of sex-associated genomic differences in cutaneous melanoma. The study integrates somatic mutation data from TCGA-SKCM and multiple cBioPortal melanoma cohorts using R and specialized bioinformatic tools.

The main objective of this project was to evaluate whether men and women with melanoma present differences in tumor mutational burden (TMB), mutational frequency patterns, and differentially mutated genes.

---

# Datasets

## TCGA

Data were downloaded using the `TCGAbiolinks` package from:

- Project: TCGA-SKCM
- Data category: Simple Nucleotide Variation
- Data type: Masked Somatic Mutation

Clinical data including patient sex were also retrieved from TCGA.

## cBioPortal

The following melanoma studies were integrated:

- DFCI_2015
- Broad_2012
- SM_Broad_2012
- SM_Broad_2014
- Yale_2012

Mutation and clinical files were downloaded from cBioPortal and harmonized using patient identifiers.

---

# Bioinformatic pipeline

The pipeline included the following steps:

1. Download and preprocessing of mutation data
2. Integration of clinical information
3. Harmonization of patient identifiers
4. Filtering of coding non-synonymous variants
5. Construction of MAF objects using `maftools`
6. Tumor Mutational Burden (TMB) calculation
7. Frequency analysis of mutated genes by sex
8. Differential mutation analysis using `mafCompare()`
9. Visualization with:
   - coBarplot
   - Volcano plots
   - Venn diagrams
10. Exploratory generalized linear model (GLM) analysis
11. Export of reproducible outputs and session information

---

# Software and packages

## Language

- R

## Main packages

- TCGAbiolinks
- maftools
- dplyr
- ggplot2
- readr
- stringr
- ggrepel
- VennDiagram
- broom
- purrr

---

# Repository structure

```text
├── TFM_V1.Rmd
├── README.md