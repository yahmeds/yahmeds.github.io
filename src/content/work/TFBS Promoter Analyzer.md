---
title: TFBS Promoter Analyzer
publishDate: 2025-03-28 00:00:00
img: /assets/biojpg.jpg
img_alt: Visualization of transcription factor binding sites in gene promoters
description: |
  A Python-based bioinformatics tool to retrieve, analyze, and visualize potential transcription factor binding sites (TFBS) in gene promoter sequences using JASPAR motifs.
tags:
  - Python
  - Bioinformatics
  - Data Visualization
  - NCBI
---

[🔗 View the GitHub repository](https://github.com/yahmeds/TFBS-Promoter-Analyzer)

## Overview

This project is a gene promoter analysis tool developed in Python. It retrieves mRNA-linked promoter sequences using the NCBI API, analyzes them with Position Weight Matrices (PWM) from the JASPAR database, and detects likely transcription factor binding sites (TFBS). 

The tool outputs structured JSON data and includes an HTML interface to visualize the results interactively.

---

## Key Features

- Automated retrieval of promoter sequences from mRNA IDs (via NCBI)
- PWM to PSSM conversion for accurate scanning
- Identification of binding sites based on score thresholds
- JSON-based result output (matches, windows, parameters)
- Interactive data visualization via HTML
- Comprehensive unit testing with `make test`

---

## Visualization Highlights

The `drawTFBS()` function dynamically maps detected TFBS and their associated windows:

- **Blue dots**: TFBS sites (color intensity reflects match score)
- **Red boxes**: Highlighted promoter windows with significant TFBS activity
- **Hover feature**: Displays additional info for each binding site
![alt](/assets/Affichage_basique.png)
---

## Technologies Used

- **Python** (main scripting and analysis)
- **Biopython** (NCBI API, FASTA parsing)
- **JASPAR** (PWM motif database)
- **HTML + JS** (custom visualization)
- **Makefile** (test automation)

---

## Sample Command

```bash
python3 src/putativeTFBS.py -m data/MA0083.3.jaspar -t -20 -s 10 NM_000451 NM_007389 -o output
```

## JSON Output Structure

- **`parameters`**: Metadata about the run
- **`matches`**: Individual TFBS sites with score and position
- **`windows`**: Grouped binding sites by window range

---

## Final Notes

This project demonstrates practical applications of bioinformatics through coding — from data retrieval to visual interpretation of genomic features.  
It emphasizes clean modular code, biologically relevant results, and clear visualization for interpretability.

