# scRNA and scATAC analysis of sarcoidosis patient PBMCs
This repository contains the code used for the analysis of scRNA and scATAC data generated from the same PBMC samples of 12 sarcoidosis patients and 6 healthy controls. Files are split into major parts of the analysis, starting from cellranger output. Filtered count matrix and cell/biological sample metadata as well as fragments files are submitted at GEO (GSE330562 and GSE330563).

## Outline of each file in order or the performed analysis:
### sarcoidosis_rna.qmd:
QC-filtering of scRNA-seq cellranger outputs, dimensional reduction, harmony integration and clustering, celltype annotation using marker gene expression and pseudobulk analysis of annotated cell types.

### sarcoidosis_atac_1.qmd:
Merging of scATAC-seq cellranger outputs and recalculation of peak matrices, dimensional reduction, harmony integration and clustering, Gene activity inference, label transfer from scRNA-seq sata and validation using marker gene activity

### sarcoidosis_pycistopic.pypi:
Pseudobulk-based peak calling and generation of consensus peaks following PyCisTopic vignette.

### sarcoidosis_atac_2.qmd:

### scenicplus_rna.pypi:
preprocessing of scRNA-seq seurat object to use in SCENIC+

### scenicplus.pypi:
using the scATAC-seq pycistopic object and the scRNA-seq anndata object to run SCENIC+

### RNA_and_ATAC_visualization.qmd
Joint RNA/ATAC/SCENIC+ analysis and data visualization for the manuscript.
