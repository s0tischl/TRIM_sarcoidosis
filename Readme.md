# scRNA and scATAC analysis of sarcoidosis patient PBMCs
This repository contains the code used for the analysis of scRNA and scATAC data generated from the same PBMC samples of 12 sarcoidosis patients and 6 healthy controls. Files are split into major parts of the analysis, starting from cellranger output. Filtered count matrix and cell/biological sample metadata as well as fragments files are submitted at GEO ([GSE330562](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE330562) and [GSE330563](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE330563)).

Thanks to [Martin Schlüter](https://gruene.social/@maddin) for teaching me the use of the command line!

## Outline of each file in order of the performed analysis:
### sarcoidosis_rna.qmd:
QC-filtering of scRNA-seq cellranger outputs, dimensional reduction, harmony integration and clustering, celltype annotation using marker gene expression and pseudobulk analysis of annotated cell types.

### sarcoidosis_atac_1.qmd:
Merging of scATAC-seq cellranger outputs and recalculation of count matrix, dimensional reduction, harmony integration and clustering, Gene activity inference, label transfer from scRNA-seq sata and validation using marker gene activity.

### sarcoidosis_pycistopic.html:
Pseudobulk-based peak calling and generation of consensus peaks following PyCisTopic vignette. Preparation of a PyCisTopic object for use in SCENIC+.

### sarcoidosis_atac_2.qmd:
Re-calculation of count matrix based on consensus peaks generated with PyCisTopic and pseudobulk analysis of annotated cell types.

### scenicplus_rna.html:
Preparation of a scRNA-seq anndata object to use in SCENIC+.

### bocklab_sarcoidosis.qmd:
Preparation of public dataset from [Krausgruber et al 2023](https://www.cell.com/immunity/fulltext/S1074-7613(23)00024-9) and pseudobulk analysis of skin macrophages and CD4 T cells.

### RNA_and_ATAC_visualization.qmd
Joint RNA/ATAC/SCENIC+ analysis and data visualization for the manuscript.
