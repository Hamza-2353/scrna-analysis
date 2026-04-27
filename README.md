# Single-Cell RNA-Seq Analysis Pipeline

This repository contains a comprehensive scRNA-seq analysis workflow, implemented in Python using the **Scanpy** framework. The pipeline follows standard bioinformatics best practices, from raw data preprocessing and quality control to cell clustering and marker gene identification.

## Project Description
This project demonstrates the end-to-end analysis of single-cell RNA sequencing data. It covers the following key analytical steps:
* **Quality Control:** Filtering cells based on gene counts and mitochondrial gene content.
* **Normalization & Scaling:** Scaling data to unit variance and log-transforming expression values.
* **Feature Selection:** Identifying highly variable genes (HVGs) to drive dimensionality reduction.
* **Dimensionality Reduction:** Utilizing Principal Component Analysis (PCA) and UMAP for visualization.
* **Clustering:** Performing Leiden clustering to identify distinct cell populations.
* **Annotation:** Identifying marker genes for biological interpretation.

## Workflow
The primary analysis is located in the `notebooks/` folder:
1. `01_preprocessing_and_qc.ipynb`: Initial data loading and filtering.
2. `02_clustering_and_visualization.ipynb`: Dimension reduction, clustering, and DEG analysis.

## Prerequisites
This analysis requires a Python environment with the following dependencies:
* `scanpy`
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`

To set up your environment, run:
```bash
pip install scanpy pandas numpy matplotlib seaborn
