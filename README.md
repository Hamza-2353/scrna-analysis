# scRNA-seq Analysis

This repository contains three single-cell RNA sequencing (scRNA-seq) analysis projects completed as part of a bioinformatics assignment. Each task is organized in its own sub-repository with complete code, outputs, and documentation.

---

## Repository Structure

```
scrna-analysis/
├── 01-preprocessing/          ← 10X Single-Cell RNA pre-processing (Galaxy tutorial)
├── 02-basic-scrna-tutorial/   ← Basic scRNA-seq analysis with Scanpy
└── 03-anndata/                ← AnnData object exploration and manipulation
```

---

## Sub-Repositories

### 1. Pre-processing of 10X Single-Cell RNA Datasets
**Folder:** `01-preprocessing/`

Covers quality control, filtering, normalization, and preparation of raw 10X Genomics scRNA-seq data using Scanpy and standard bioinformatics tools. Based on the [Galaxy Project scRNA-seq pre-processing tutorial](https://training.galaxyproject.org/training-material/topics/single-cell/tutorials/scrna-preprocessing-tenx/tutorial.html).

**Key steps:** Load 10X data → QC metrics → Filter cells & genes → Normalize → Log-transform → Highly variable genes → PCA → Save output

---

### 2. Basic scRNA-seq Tutorial
**Folder:** `02-basic-scrna-tutorial/`

End-to-end scRNA-seq analysis workflow including clustering, UMAP visualization, and marker gene identification using Scanpy. Based on the [official Scanpy tutorial](https://github.com/scverse/scanpy-tutorials/blob/main/basic-scrna-tutorial.ipynb).

**Key steps:** Load preprocessed data → Dimensionality reduction → Clustering (Leiden) → UMAP → Marker genes → Cell type annotation

---

### 3. AnnData Tutorial
**Folder:** `03-anndata/`

Exploration of the AnnData data structure used throughout the scverse ecosystem. Covers creating, accessing, modifying, and saving AnnData objects. Based on the [AnnData getting-started tutorial](https://anndata.readthedocs.io/en/latest/tutorials/notebooks/getting-started.html) and the [scverse AnnData tutorial](https://scverse-tutorials.readthedocs.io/en/latest/notebooks/anndata_getting_started.html).

**Key steps:** Create AnnData objects → Access `.X`, `.obs`, `.var`, `.obsm` → Subset & concatenate → Read/write `.h5ad` files

---

## How to Run

All notebooks are designed to run in **Google Colab** (no local setup needed) or locally with **Jupyter Notebook**.

### Option A — Google Colab (recommended)
Open each `.ipynb` file in the sub-folder, click the **"Open in Colab"** badge, and run all cells.

### Option B — Local setup
```bash
pip install scanpy anndata matplotlib seaborn pandas numpy
jupyter notebook
```

---

## Tools & Libraries

| Library | Version | Purpose |
|---|---|---|
| `scanpy` | ≥1.9 | scRNA-seq analysis |
| `anndata` | ≥0.9 | Data structure |
| `matplotlib` | ≥3.5 | Plotting |
| `seaborn` | ≥0.12 | Statistical visualization |
| `pandas` | ≥1.5 | Data manipulation |
| `numpy` | ≥1.23 | Numerical computing |

---

## Dataset

All tasks use the **PBMC 3K dataset** from 10X Genomics — a standard benchmark dataset of ~3,000 peripheral blood mononuclear cells.

- [Download PBMC 3K dataset](https://cf.10xgenomics.com/samples/cell/pbmc3k/pbmc3k_filtered_gene_bc_matrices.tar.gz)
- Scanpy also provides a built-in loader: `sc.datasets.pbmc3k()`

---

## Author

**Hamza** | Bioinformatics Assignment | 2026
