# Task 2 — Basic scRNA-seq Tutorial

End-to-end single-cell RNA-seq analysis workflow using **Scanpy**, covering clustering, UMAP visualization, and marker gene identification.

**Reference:** [Scanpy Basic scRNA-seq Tutorial](https://github.com/scverse/scanpy-tutorials/blob/main/basic-scrna-tutorial.ipynb)

---

## What This Notebook Does

| Step | Description |
|---|---|
| 1. Load data | Load the pre-processed PBMC 3K AnnData from Task 1 |
| 2. Neighborhood graph | Compute k-nearest neighbors graph |
| 3. UMAP | Compute UMAP 2D embedding |
| 4. Clustering | Leiden community detection algorithm |
| 5. Marker genes | Find differentially expressed genes per cluster |
| 6. Visualization | Dot plots, violin plots, UMAP colored by cluster & gene |
| 7. Cell type annotation | Manually annotate clusters using known marker genes |

---

## Outputs & Plots Generated

| File | Description |
|---|---|
| `umap_clusters.png` | UMAP colored by Leiden cluster |
| `umap_markers.png` | UMAP colored by key marker genes |
| `dotplot_markers.png` | Dot plot of marker gene expression per cluster |
| `violin_markers.png` | Violin plot of top marker genes |
| `rank_genes_groups.png` | Top differentially expressed genes per cluster |
| `pbmc3k_clustered.h5ad` | Final annotated AnnData object |

---

## Key Marker Genes Used for Annotation

| Cell Type | Marker Genes |
|---|---|
| CD4 T cells | IL7R, CCR7 |
| CD14 Monocytes | CD14, LYZ |
| B cells | MS4A1 |
| CD8 T cells | CD8A |
| NK cells | GNLY, NKG7 |
| Dendritic cells | FCER1A, CST3 |
| Megakaryocytes | PPBP |

---

## How to Run

### Google Colab
Open `02_basic_scrna_tutorial.ipynb` in Colab and run all cells.
> Make sure `pbmc3k_preprocessed.h5ad` from Task 1 is available, or the notebook will regenerate it automatically.

### Local
```bash
pip install scanpy leidenalg matplotlib seaborn
jupyter notebook 02_basic_scrna_tutorial.ipynb
```

---

## Reference

Wolf, F.A., Angerer, P. & Theis, F.J. SCANPY: large-scale single-cell gene expression data analysis. *Genome Biology* 19, 15 (2018). https://doi.org/10.1186/s13059-017-1382-0
