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
* `notebooks/`: Contains the Jupyter notebooks for the analysis.

## Prerequisites
To run this analysis, you will need a Python environment with the following dependencies:
* `scanpy`, `pandas`, `numpy`, `matplotlib`, `seaborn`

## Usage
1. Clone this repository: `git clone https://github.com/Hamza-2353/scrna-analysis.git`
2. Navigate to the `notebooks/` folder.
3. Open the Jupyter notebook and execute the cells sequentially.

## Data Source
The data used for this analysis was sourced from the [Scanpy Tutorials](https://github.com/scverse/scanpy-tutorials/).

## License
This project is licensed under the MIT License.
