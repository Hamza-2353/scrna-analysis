# Task 2 — Basic scRNA-seq Tutorial

End-to-end single-cell RNA-seq analysis workflow using **Scanpy**, covering clustering, UMAP visualization, and marker gene identification.

**Reference:** [Scanpy Basic scRNA-seq Tutorial](https://github.com/scverse/scanpy-tutorials/blob/main/basic-scrna-tutorial.ipynb)

---

## Analysis Results
The following visualizations were generated during the workflow and are available in the `results/` folder:

| File | Description |
|---|---|
| `cell_filtering.png` | Quality control metrics |
| `cell_type_annotation.png` | Manual cell type labels |
| `clustering.png` | Leiden clustering overview |
| `clusters.png` | UMAP clusters |
| `dimensionality_reduction.png` | PCA results |
| `feature_selection.png` | Highly variable genes |
| `filtering.png` | Pre-processing effects |
| `marker_gene.png` | Differential expression analysis |
| `markers.png` | Key marker genes |
| `nearest_neighbour.png` | Neighborhood graph |
| `plot.png` | Summary visualization |
| `quality_control.png` | QC distributions |
| `scatterplot_dimensionality.png` | Dimensionality reduction plot |

---

## Workflow Summary

| Step | Description |
|---|---|
| 1. Load data | Load the pre-processed PBMC 3K AnnData |
| 2. Neighborhood graph | Compute k-nearest neighbors graph |
| 3. UMAP | Compute UMAP 2D embedding |
| 4. Clustering | Leiden community detection algorithm |
| 5. Marker genes | Find differentially expressed genes per cluster |
| 6. Visualization | Dot plots, violin plots, UMAP colored by cluster & gene |
| 7. Cell type annotation | Manual annotation using known markers |

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

### Local
```bash
pip install scanpy leidenalg matplotlib seaborn
jupyter notebook 02_basic_scrna_tutorial.ipynb
