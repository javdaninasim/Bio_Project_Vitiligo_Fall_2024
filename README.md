<div align="center">

<h1 align="center">🧬 Vitiligo — Computational Biology Analysis</h1>
<h3 align="center">Bioinformatics Project | Sharif University of Technology</h3>

[**GitHub**](https://github.com/javdaninasim/Bio_Project_Vitiligo_Fall_2024) &nbsp; ⬩ &nbsp; [**University**](https://sharif.edu/)

</div>

---

### 📚 Project Overview

```python
class VitiligoProject:
    def __init__(self):
        self.institution = "Sharif University of Technology"
        self.department = "Computational Biology"
        self.semester = "Fall 2024"
        self.focus = "Transcriptomic Analysis & Pathway Identification"
        
    def objectives(self):
        return {
            "Disease Understanding": "Autoimmune mechanisms in Vitiligo pathogenesis",
            "Data Analysis": "Differential expression & gene set enrichment",
            "Pathway Mapping": "Biological pathway identification (Reactome)",
            "Insights": "Therapeutic targets and immunological pathways"
        }
    
    def mission(self):
        return "Identify dysregulated genes and pathways in Vitiligo through systems biology approaches."
```

---

### 📂 Repository Structure

```
Bio_Project_Vitiligo_Fall_2024/
│
├── 📊 Results and Scripts/
│   │
│   ├── 1️⃣ Raw data analysis/
│   │   ├── script 12.r                           # Data normalization and quality control (12 samples)
│   │   ├── script 18.r                           # Data normalization and quality control (18 samples)
│   │   ├── all genes 12.tsv                      # Raw expression matrix (12 samples, all genes)
│   │   ├── all genes 18.tsv                      # Raw expression matrix (18 samples, all genes)
│   │   ├── Boxplot of samples 12.jpg             # Quality control visualization (12 samples)
│   │   └── Boxplot of samples 18.jpg             # Quality control visualization (18 samples)
│   │
│   ├── 2️⃣ Significance analysis/
│   │   ├── significant genes 12.tsv              # Differentially expressed genes (12 samples)
│   │   ├── significant genes 18.tsv              # Differentially expressed genes (18 samples, FDR < 0.05)
│   │   ├── Volcano plot 12.mhtml                 # Interactive volcano plot (log2FC vs p-value, 12 samples)
│   │   ├── Volcano plot 18.mhtml                 # Interactive volcano plot (log2FC vs p-value, 18 samples)
│   │   ├── Mean Difference plot 12.mhtml         # MA plot for fold-change visualization (12 samples)
│   │   ├── Mean Difference plot 18.mhtml         # MA plot for fold-change visualization (18 samples)
│   │   ├── UMAP clusters 12.jpg                  # Dimensional reduction & sample clustering (12 samples)
│   │   ├── UMAP clusters 18.jpg                  # Dimensional reduction & sample clustering (18 samples)
│   │   └── UMAP clusters all.jpg                 # Combined UMAP visualization (all samples)
│   │
│   ├── 3️⃣ Gene Set analyses/
│   │   ├── Enrichment table.csv                  # GO term enrichment statistics & p-values
│   │   ├── Enrichment bar plot.png               # Gene ontology enrichment visualization
│   │   ├── Ontology plot.png                     # Hierarchical ontology relationship diagram
│   │   └── SDE gene symbols 30.csv               # Top 30 significantly dysregulated genes
│   │
│   └── 4️⃣ Pathway analysis/
│       │
│       ├── GSA/                                  # Gene Set Analysis (GSA) results
│       │   ├── Pathway analysis of significantly regulated genes.pdf
│       │   ├── Filtered Pathways (Reactome visualization).png
│       │   ├── filtered Voronoi visualization (flattened).jpg
│       │   └── filtered Voronoi visualization (hierarchical).jpg
│       │
│       └── Set Enrichment analysis/               # Gene Set Enrichment Analysis (GSEA) results
│           ├── Pathway analysis of overrepresented genes.pdf
│           ├── Pathways (Reactome visualization) 30.png
│           ├── Pathways (Reactome visualization) 30.svg
│           ├── Filtered Pathways (Reactome visualization) 30.png
│           ├── Voronoi visualization (flattened) 30.jpg
│           ├── Voronoi visualization (hierarchical) 30.jpg
│           ├── filtered Voronoi visualization (flattened) 30.jpg
│           └── filtered Voronoi visualization (hierarchical) 30.jpg
│
├── 📑 Vitiligo Lecture.pptx                      # Project presentation slides
└── 📄 Vitiligo.pdf                               # Complete written report

```

---

### 🔬 Analysis Breakdown

| Phase | Component | Input | Output | Purpose |
| :---: | :--- | :--- | :--- | :--- |
| **1** | **Raw Data Analysis** | Gene expression matrices | Normalized expression profiles | Quality control & normalization |
| **2** | **Significance Testing** | Normalized expression | DEG lists, Volcano/MA plots | Identify dysregulated genes |
| **3** | **Gene Set Analysis** | DEG symbols | GO terms, Enrichment table | Biological process identification |
| **4** | **Pathway Analysis** | DEG sets | Reactome pathways, visualizations | Systems-level pathway mapping |

---

### 📝 Detailed Analysis Descriptions

#### **1. Raw Data Analysis** 📊

**Files:** `Results and Scripts/1 Raw data analysis/`

**R Scripts:**
- `script 12.r` - Processes 12-sample dataset
- `script 18.r` - Processes 18-sample dataset

**Workflow:**
1. **Data Loading** – Import raw gene expression matrices (TSV format)
2. **Quality Control** – Remove outliers and low-expressed genes
3. **Normalization** – Quantile normalization or TMM normalization
4. **Visualization** – Boxplots showing expression distributions across samples

**Input Data:**
- `all genes 12.tsv` – Expression matrix: 12 samples × ~20,000 genes
- `all genes 18.tsv` – Expression matrix: 18 samples × ~20,000 genes

**Output Visualizations:**
- Boxplot distributions showing normalization effectiveness
- Quality metrics for each sample
- Identification of potential batch effects

**Key Metrics:** Mean expression, expression range, coefficient of variation

---

#### **2. Significance Analysis** 🔍

**Files:** `Results and Scripts/2 Significance analysis/`

**Analytical Approach:**
- Differential Expression Analysis using **limma** (Linear Models for Microarray data)
- Statistical tests: t-test with Benjamini-Hochberg multiple testing correction
- Significance threshold: **FDR < 0.05** and **|log2FC| > 1.0**

**Output Files:**
- `significant genes 12.tsv` – DEG list (12-sample comparison)
- `significant genes 18.tsv` – DEG list (18-sample comparison, ~30 DEGs identified)

**Interactive Visualizations:**
- **Volcano plots** (MHTML):
  - X-axis: log₂(Fold Change)
  - Y-axis: -log₁₀(p-value)
  - Red points: Upregulated genes (FC > 2)
  - Blue points: Downregulated genes (FC < 0.5)
  
- **MA plots** (Mean-Difference plots):
  - X-axis: Mean expression level
  - Y-axis: log₂(Fold Change)
  - Shows fold change distribution

- **UMAP Clustering:**
  - Sample-level dimensionality reduction
  - Case vs. control group separation
  - Shows clustering quality and batch effects

**Key Findings:**
- 18-sample analysis identified ~30 significantly dysregulated genes
- UMAP visualizations confirm case/control stratification

---

#### **3. Gene Set Analysis** 🎯

**Files:** `Results and Scripts/3 Gene Set analyses/`

**Methodology:**
- **Tool:** clusterProfiler (Bioconductor R package)
- **Databases:** Gene Ontology (GO) – Biological Process, Molecular Function, Cellular Component
- **Statistical Test:** Hypergeometric test (Fisher's exact)
- **Cutoff:** FDR-adjusted p-value < 0.05

**Output Files:**
- `Enrichment table.csv` – GO term enrichment results with statistics:
  - GO ID, term name, p-value, q-value, gene count
  - Example enriched terms: immune response, T-cell activation, cytokine signaling

- `SDE gene symbols 30.csv` – Top 30 significantly dysregulated genes
  - Gene symbols, fold changes, adjusted p-values
  - Manually curated list for further investigation

**Visualizations:**
- **Enrichment bar plot** – Top enriched GO terms ranked by significance
- **Ontology plot** – Hierarchical relationships between enriched terms
  - Shows parent-child GO term connections
  - Identifies central biological themes

**Biological Insights:**
- Enriched pathways related to immune response and inflammation
- Indicates T-cell-mediated autoimmune mechanisms
- Highlights skin barrier function genes

---

#### **4. Pathway Analysis** 🔗

**Files:** `Results and Scripts/4 Pathway analysis/`

**Two complementary approaches:**

**A. Gene Set Analysis (GSA)** – `GSA/` folder
- **Input:** Significantly dysregulated genes (strict FDR cutoff)
- **Database:** Reactome pathway database
- **Focus:** Pathway over-representation analysis

**Output:**
- `Pathway analysis of significantly regulated genes.pdf` – Detailed pathway report
- **Visualizations:**
  - Filtered Reactome pathway diagrams
  - Voronoi flattened/hierarchical layouts
  - Highlights interactions between altered genes

**B. Set Enrichment Analysis (GSEA)** – `Set Enrichment analysis/` folder
- **Input:** Ranked gene list (by fold-change and p-value)
- **Method:** Rank-based pathway enrichment (doesn't require arbitrary cutoff)
- **Parameter:** Top 30 genes analyzed

**Outputs:**
- `Pathway analysis of overrepresented genes.pdf` – Comprehensive GSEA report
- **Pathway Visualizations (Reactome):**
  - Pathways (PNG, SVG formats)
  - Shows interconnected signaling cascades
  - Colored nodes indicate dysregulated genes
  
- **Voronoi Diagrams (Multiple layouts):**
  - Flattened layout: Linear pathway representation
  - Hierarchical layout: Tree-like pathway organization
  - Shows pathway topology and gene interactions

**Key Pathway Findings:**
- **Immune pathways:** TCR signaling, immune activation cascades
- **Inflammatory mediators:** Cytokine production pathways
- **Oxidative stress:** ROS generation and antioxidant response
- **Skin-specific:** Melanocyte differentiation and skin barrier pathways

---

### 🧬 Technology Stack

<div align="left">
  <img src="https://img.shields.io/badge/R-1A1A1A?style=for-the-badge&logo=r&logoColor=276DC3" alt="R" />
  <img src="https://img.shields.io/badge/Bioconductor-1A1A1A?style=for-the-badge&logo=bioinformatics&logoColor=4A90E2" alt="Bioconductor" />
  <img src="https://img.shields.io/badge/PowerPoint-1A1A1A?style=for-the-badge&logo=microsoft-powerpoint&logoColor=D24726" alt="PowerPoint" />
  <img src="https://img.shields.io/badge/Reactome-1A1A1A?style=for-the-badge&logo=database&logoColor=FF6B6B" alt="Reactome" />
</div>

<br>

> **Core Packages:** `limma` ⬩ `clusterProfiler` ⬩ `ggplot2` ⬩ `dplyr` ⬩ `biomaRt` ⬩ `ReactomePA`

---

### 🔄 Data Analysis Workflow

```
Raw Expression Data (RNA-seq / Microarray)
         ↓
    [Data Normalization & QC]  ← Scripts 1 & 2
         ↓
    Normalized Expression Matrix
         ↓
    [Differential Expression Analysis]  ← Volcano plots, MA plots, UMAP
         ↓
    Significantly Dysregulated Genes
         ↓
    ┌────────────────────────┬─────────────────────────┐
    ↓                        ↓
[Gene Set Analysis]    [Set Enrichment Analysis]
(GO Terms)             (Pathway Analysis)
    ↓                        ↓
[GO Enrichment]        [Reactome Pathways]
    ↓                        ↓
Biological Processes   Molecular Mechanisms
& Functions            & Therapeutic Targets
```

---

### 💡 Key Findings Summary

| Analysis | Major Findings |
| :--- | :--- |
| **Differentially Expressed Genes** | ~30 genes significantly altered (FDR < 0.05); mix of up- and downregulated |
| **Gene Ontology Enrichment** | Immune response, T-cell activation, cytokine signaling, apoptosis |
| **Pathway Analysis** | TCR signaling, JAK-STAT pathway, TNF pathway, NF-κB pathway |
| **Biological Relevance** | Evidence of autoimmune T-cell-mediated destruction of melanocytes |
| **Therapeutic Targets** | Immune checkpoint genes, apoptosis regulators, oxidative stress markers |

---

### 🚀 How to Use This Repository

1. **Understand the Disease:** Read `Vitiligo.pdf` for comprehensive background
2. **Review Presentation:** View `Vitiligo Lecture.pptx` for project overview
3. **Explore Raw Data:** Check `1 Raw data analysis/` for data quality and normalization
4. **Examine DEGs:** Open Volcano/MA plots in `2 Significance analysis/` for dysregulated genes
5. **Investigate Processes:** View GO enrichment plots in `3 Gene Set analyses/`
6. **Study Pathways:** Analyze Reactome visualizations in `4 Pathway analysis/` subfolders

---

### 📖 Technical Details

**Data Characteristics:**
- Two datasets: 12-sample and 18-sample cohorts
- Control group vs. Vitiligo patient samples
- RNA-seq or microarray expression data

**Analysis Methods:**
- Quality control: Boxplots, expression distribution analysis
- Normalization: Quantile or TMM normalization
- Statistics: Empirical Bayes t-test (limma)
- Multiple testing correction: Benjamini-Hochberg FDR
- Enrichment: Hypergeometric test
- Visualization: UMAP clustering, interactive plots (MHTML), Reactome pathway mapping

**File Formats:**
- `TSV` – Tab-separated gene expression matrices
- `CSV` – Comma-separated results tables
- `JPG/PNG/SVG` – Publication-quality visualizations
- `MHTML` – Interactive web-based plots
- `PDF` – Comprehensive analysis reports
- `R` – Reproducible analysis scripts

---

### ℹ️ Project Information

| Detail | Information |
| :--- | :--- |
| **Institution** | Sharif University of Technology, Dept. of Computer Engineering |
| **Course** | Computational Biology |
| **Semester** | Fall 2024 |
| **Project Type** | Transcriptomic analysis + systems biology |
| **Languages** | R, RMarkdown |
| **Analysis Type** | Differential expression + pathway enrichment |
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=FFC0CB&height=100&section=footer" width="100%"/>
</div>
