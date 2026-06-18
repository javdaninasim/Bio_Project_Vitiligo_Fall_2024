# Bioinformatics Programming Homeworks — Fall 2024

> Coursework repository for the **Bioinformatics** course at Sharif University of Technology, Fall 2024.  
> **Author:** Nasim Javdani · [GitHub](https://github.com/javdaninasim) · [LinkedIn](https://linkedin.com/in/nasim-javdani-810a9932a)

---

## Overview

This repository contains three programming homework assignments for the Bioinformatics course, implemented in Python. The assignments cover foundational algorithms in computational biology — from sequence analysis to phylogenetic tree construction.

---

## Repository Structure

```
BioInformatics_PHW_Fall_2024/
├── BioInformatics_PHW_NeighborJoining_Fall_2024/
├── BioInformatics_PHW_Query_Fall_2024/
└── BioInformatics_PHW_SequenceAlignment_Fall_2024/
```

---

## Assignments

### 1. Sequence Alignment
Implementation of classical sequence alignment algorithms used to find the optimal alignment between biological sequences (DNA, RNA, or protein).

Key topics:
- **Global Alignment** — Needleman-Wunsch algorithm
- **Local Alignment** — Smith-Waterman algorithm
- Scoring matrices (e.g., BLOSUM, PAM)
- Gap penalties (linear and affine)

### 2. Biological Database Query
Programmatic querying of bioinformatics databases to retrieve, filter, and process biological sequence data.

Key topics:
- Interfacing with databases such as NCBI (via Biopython's Entrez module)
- Parsing FASTA and GenBank formats
- Filtering and organizing retrieved sequences for downstream analysis

### 3. Neighbor Joining (Phylogenetic Tree Construction)
Implementation of the **Neighbor Joining (NJ)** algorithm for constructing phylogenetic trees from a distance matrix derived from multiple sequence alignments.

Key topics:
- Computing pairwise distance matrices
- Iterative tree construction via the NJ method
- Tree visualization

---

## Technologies

| Tool | Purpose |
|---|---|
| Python 3 | Primary language |
| Biopython | Sequence handling, database access, alignment |
| NumPy | Numerical operations and matrix computation |
| Matplotlib | Phylogenetic tree and result visualization |

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/javdaninasim/BioInformatics_PHW_Fall_2024.git
   cd BioInformatics_PHW_Fall_2024
   ```

2. Install dependencies:
   ```bash
   pip install biopython numpy matplotlib
   ```

3. Navigate into any assignment folder and run the corresponding Python script or notebook.

---

## Course Info

- **Course:** Bioinformatics
- **Institution:** Sharif University of Technology, Department of Computer Engineering
- **Presenter:** Ali Sharifi Zarchi
- **Semester:** Fall 2024
