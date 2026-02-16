# Gastruloid Project

## Requirements

```
scanpy==1.11.5
scvi-tools==1.0.3
treeclust==0.0.1
moscot==0.5.0
scib-metrics==0.1.0
harmonypy==0.0.10
distinctipy==1.3.4
scmappy==0.3
umap-learn==0.5.9.post2
pandas==2.3.3
numpy==2.3.5
scipy==1.16.3
scikit-learn==1.7.2
matplotlib==3.10.7
seaborn==0.13.2
plotly==6.5.0
```

where treeclust is deposited in [https://github.com/gatocor/treeclust](https://github.com/gatocor/treeclust).

## Tracked Files

### Analysis Notebooks

| File | Description |
|------|-------------|
| `analysis_by_batch.ipynb` | Batch-wise preprocessing pipeline including QC filtering, normalization, PCA, UMAP, and clustering using scanpy and scVI. Reads parameters from `parameters_by_batch.csv`. |
| `analysis_clustering.ipynb` | Consensus clustering using treeclust with bootstrapped PCA and Leiden algorithm for robust cell population identification. |
| `analysis_annotation.ipynb` | Cell type annotation pipeline using hierarchical clustering and marker-based annotation propagation. |
| `analysis_integrated_full.ipynb` | Full dataset integration across all timepoints using batch correction (Harmony) and joint embedding. |
| `analysis_integrated_full_plot.ipynb` | Visualization of integrated full dataset with UMAP plots and cell type overlays. |
| `analysis_OT.ipynb` | Optimal transport analysis using moscot to compute cell fate transitions between consecutive timepoints (48h→72h→96h→120h→144h). |
| `analysis_OT_plot.ipynb` | Sankey diagram visualization of optimal transport transitions. |
| `analysis_projection_time.ipynb` | Temporal projection analysis for mapping cells across developmental stages. |

### Reference Data

| File | Description |
|------|-------------|
| `cell_cycle_G1_S.txt` | Comma-separated list of mouse G1/S phase marker genes for cell cycle scoring. |
| `cell_cycle_G2_M.txt` | Comma-separated list of mouse G2/M phase marker genes for cell cycle scoring. |
| `markers.csv` | List of marker genes used for visualization and cell type identification. |
| `parameters_by_batch.csv` | QC parameters per batch/sample: count thresholds, gene filters, mitochondrial fraction limits, PCA components, and clustering settings. |
