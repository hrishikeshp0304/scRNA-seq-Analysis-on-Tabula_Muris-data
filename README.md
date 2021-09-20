# scRNA_seq-Analysis

### Dataset link - https://www.kaggle.com/hrishikeshp/tabula-muris
* [Tabula Muris](https://tabula-muris.ds.czbiohub.org/) is a compendium of single-cell transcriptome data from the model organism Mus musculus, containing nearly 100,000 cells from 20 organs and tissues. 
* The data allow for direct and controlled comparison of gene expression in cell types shared between tissues, such as immune cells from distinct anatomical locations.
* **This data consists of an expression matrix where each column corresponds to a gene (or transcript) and each row corresponds to a single cell and a table of metadata describing each cell.**


### 0. Theory - Introduction to single-cell RNA-seq - [Kaggle Link](https://www.kaggle.com/hrishikeshp/0-single-cell-rna-seq-introduction-workflow) 
- Covers most of the theoretical concepts about Bulk RNA-seq, scRNA-seq and Computational Analysis.

### 1. AnnData and Preprocessing spike-ins - [Kaggle Link](https://www.kaggle.com/hrishikeshp/1-exploring-anndata-preprocessing) 
- Theory behind AnnData objects
- Exploring a test anndata
- Creating Anndata from the csv files in the dataset
- Preprocessing the labeling spike-ins


### 2. Quality Control in Single cell RNA-seq data - [Kaggle Link](https://www.kaggle.com/hrishikeshp/2-quality-control-in-single-cell-rna-seq-data) 
- Calculated the quality control metrices across cells and genes.
- Quality control in cells by removing cells with less total gene count, less unique genes and giving more spike-ins.
- Quality control in genes by removing genes which occur in less unique cells as well as those genes having less total cells.

### 3. Normalization & PCA - [Kaggle Link](https://www.kaggle.com/hrishikeshp/3-normalization-and-pca-in-scrna-seq-data) 
- Directly applying PCA on quality controlled data
- Applying CPM normalization and then PCA
- Normalizing each cell by total counts over all genes and excluding highly_expressed genes and then PCA
- Removing offending gene Rn45s and then PCA
- Final, Normalization by log1p and scaling and then PCA.
