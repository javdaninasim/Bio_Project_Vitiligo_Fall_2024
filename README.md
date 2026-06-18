# Vitiligo — Computational Biology Project, Fall 2024

> Course project for the **Computational Biology** course at Sharif University of Technology, Fall 2024.  
> **Author:** Nasim Javdani · [GitHub](https://github.com/javdaninasim) · [LinkedIn](https://linkedin.com/in/nasim-javdani-810a9932a)

---

## Overview

This project investigates **Vitiligo**, an autoimmune skin condition characterized by the loss of melanocytes and the depigmentation of skin patches. The work combines a literature-based analysis with computational approaches, including gene expression analysis and biological data processing using R.

---

## Repository Structure

```
Bio_Project_Vitiligo_Fall_2024/
├── Results and Scripts/     # R analysis scripts and generated output figures
├── Vitiligo Lecture.pptx    # Presentation slides used for the project defense
└── Vitiligo.pdf             # Final written report
```

---

## Contents

### `Results and Scripts/`
Contains the R scripts used for data analysis and the corresponding output results. Key analyses may include:
- Differentially expressed gene (DEG) analysis
- Pathway enrichment analysis
- Visualization of expression profiles (heatmaps, volcano plots)

### `Vitiligo Lecture.pptx`
The lecture/presentation slides summarizing:
- Disease background and pathology
- Genetic and immunological factors
- Computational findings and insights

### `Vitiligo.pdf`
The full written report covering:
- Introduction to Vitiligo (types, epidemiology, pathogenesis)
- Immune system involvement (T-cell mediated destruction of melanocytes)
- Genetic risk factors and relevant gene networks
- Computational analysis methodology and results
- Conclusions and potential therapeutic targets

---

## Background

Vitiligo affects roughly 1–2% of the global population. It involves a complex interplay of genetic predisposition, oxidative stress, and autoimmune T-cell activity targeting melanocytes. This project explores the molecular underpinnings using bioinformatics tools and publicly available genomic data.

---

## Technologies

| Tool | Purpose |
|---|---|
| R | Statistical analysis and bioinformatics |
| Bioconductor packages | Gene expression analysis (e.g., `limma`, `DESeq2`) |
| ggplot2 | Data visualization |
| PowerPoint | Presentation |

---

## How to Run the Scripts

1. Install R (≥ 4.0) and RStudio.
2. Install required packages:
   ```r
   install.packages(c("ggplot2", "dplyr"))
   if (!requireNamespace("BiocManager", quietly = TRUE))
       install.packages("BiocManager")
   BiocManager::install(c("limma", "DESeq2", "clusterProfiler"))
   ```
3. Open the scripts in the `Results and Scripts/` folder and run them in order.

---

## Course Info

- **Course:** Computational Biology (Bio)
- **Institution:** Sharif University of Technology, Department of Computer Engineering
- **Semester:** Fall 2024
