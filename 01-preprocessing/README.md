# scRNA-seq Pre-processing: 10X Genomics Pipeline

This repository contains the documentation and workflow associated with the **"Pre-processing of 10X Single-Cell RNA Datasets"** tutorial from the Galaxy Training Network (GTN). 

## Overview
Single-cell RNA sequencing (scRNA-seq) provides high-throughput resolution for examining cell heterogeneity. This project focuses on the initial, crucial stage of the bioinformatics pipeline: transforming raw FASTQ sequencing data into a reliable, quality-controlled count matrix.

### Key Objectives
* **Demultiplexing & Quantification:** Converting raw 10X Genomics FASTQ files into a gene-by-cell count matrix.
* **Mapping:** Using **RNA STARsolo** for efficient, high-throughput alignment of reads to the reference genome (hg19/GRCh37).
* **Quality Control (QC):** Identifying and filtering low-quality cells based on barcode rankings, mitochondrial content, and feature counts to ensure the integrity of downstream analysis.

## Pipeline Workflow & Data Visualization

The analysis follows these primary steps, supported by specific visualizations for data inspection:

1.  **Data Acquisition:** Importing sub-sampled PBMC (Peripheral Blood Mononuclear Cell) datasets and necessary annotations.
2.  **Mapping (STARsolo):** Alignment of cDNA reads while utilizing a cell barcode "whitelist" to demultiplex samples.
3.  **QC Assessment:** Investigating the STARsolo feature statistics and the generated plots to determine the number of detected cells and mapping quality.

### Data Visualizations

This project emphasizes visual QC using specific plots generated during the pre-processing stage:

| Plot Name | Visualization Description | Key Information Provided |
| :--- | :--- | :--- |
| **Barcode Rank Plot** (Elbow Plot) | A log-log plot ranking barcodes by UMI count (y-axis) vs. rank (x-axis). | Identifies the "knee" and "inflection" points used to distinguish actual cells from background noise (empty droplets). |
| **QC Scatter Plot** | Scatter plot of Total UMI count (x-axis) vs. -Log Probability (y-axis). | visualizes technical noise and provides a view of how technical metrics relate across the cell population, assisting in identifying outliers. |

## Results: Quality Control

The following plots were generated during the pre-processing stage to ensure data quality:

### Barcode Rank Plot
![Barcode Rank Plot](01-preprocessing/results/barcode_rank_plot.png)
*Figure 1: Rank of barcodes by UMI counts used to identify the "knee" and "inflection" points.*

### QC Scatter Plot
![QC Scatter Plot](01-preprocessing/results/qc_scatter_plot.png)
*Figure 2: Scatter plot of Total UMI count vs. -Log Probability to visualize technical noise and outliers.*

4.  **Matrix Refinement:** Filtering the raw matrix based on these QC thresholds to produce a high-quality dataset suitable for downstream biological interpretation.

## Tools & Resources
* **Platform:** [UseGalaxy.org](https://usegalaxy.org/)
* **Alignment Tool:** [RNA STARsolo](https://github.com/alexdobin/STAR)
* **Supporting Framework:** [Galaxy Training Network (GTN)](https://training.galaxyproject.org/training-material/)
* **Dataset:** 1k PBMCs from a Healthy Donor (10X Genomics, v3 Chemistry)

## References
* **Melsted, P. et al. (2019).** Modular and efficient pre-processing of single-cell RNA-seq. [doi:10.1101/673285](https://doi.org/10.1101/673285)
* **Tekman, M. et al. (2020).** A single-cell RNA-sequencing training and analysis suite using the Galaxy framework. *GigaScience*. [doi:10.1093/gigascience/giaa102](https://doi.org/10.1093/gigascience/giaa102)

---
