# Task 1 — Pre-processing of 10X Single-Cell RNA Datasets

This notebook covers the complete pre-processing pipeline for raw 10X Genomics single-cell RNA-seq data, following the [Galaxy Project tutorial](https://training.galaxyproject.org/training-material/topics/single-cell/tutorials/scrna-preprocessing-tenx/tutorial.html).

---

## What This Notebook Does

| Step | Description |
|---|---|
| 1. Load data | Read 10X Genomics matrix files into an AnnData object |
| 2. QC metrics | Calculate % mitochondrial genes, total counts, n_genes per cell |
| 3. QC plots | Violin plots and scatter plots for quality inspection |
| 4. Filter cells | Remove low-quality cells and doublets |
| 5. Filter genes | Remove genes detected in very few cells |
| 6. Normalize | Normalize total counts per cell to 10,000 |
| 7. Log-transform | Apply log1p transformation |
| 8. HVGs | Identify highly variable genes |
| 9. Scale | Scale data to unit variance |
| 10. PCA | Run PCA for dimensionality reduction |
| 11. Save | Save filtered AnnData to `.h5ad` file |

---

## Dataset

**PBMC 3K** — 3,000 Peripheral Blood Mononuclear Cells from 10X Genomics.

```python
# Loaded automatically in the notebook via:
import scanpy as sc
adata = sc.datasets.pbmc3k()
```

---

## How to Run

### Google Colab (easiest)
Click the badge at the top of the notebook and run all cells in order.

### Local
```bash
pip install scanpy matplotlib seaborn
jupyter notebook 01_preprocessing.ipynb
```

---

## Output Files

| File | Description |
|---|---|
| `pbmc3k_preprocessed.h5ad` | Filtered, normalized AnnData object |
| `qc_violin.png` | QC violin plot |
| `qc_scatter.png` | Scatter plot of QC metrics |
| `highly_variable_genes.png` | HVG plot |
| `pca.png` | PCA variance ratio plot |

---

## Key Parameters Used

```python
min_genes = 200        # minimum genes per cell
min_cells = 3          # minimum cells per gene
max_genes = 2500       # maximum genes per cell (doublet filter)
max_pct_mito = 5       # maximum % mitochondrial reads
n_top_genes = 2000     # number of highly variable genes
```

---

## Reference

Galaxy Training Network. *Pre-processing of 10X Single-Cell RNA Datasets.*
https://training.galaxyproject.org/training-material/topics/single-cell/tutorials/scrna-preprocessing-tenx/tutorial.html
