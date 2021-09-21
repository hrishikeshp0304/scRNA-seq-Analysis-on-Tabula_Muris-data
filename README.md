# scRNA-seq Analysis on Tabula Muris data

I have made a dataset of Tabula Muris on Kaggle, and worked on the Kaggle kernel for each of the notebooks below. They can be accessed using the links provided. 

### Dataset link - https://www.kaggle.com/hrishikeshp/tabula-muris
* [Tabula Muris](https://tabula-muris.ds.czbiohub.org/) is a compendium of single-cell transcriptome data from the model organism Mus musculus, containing nearly 100,000 cells from 20 organs and tissues. 
* The data allow for direct and controlled comparison of gene expression in cell types shared between tissues, for e.g. immune cells from distinct anatomical locations.
* The full dataset includes both high throughput but low-coverage 10X data and lower throughput but high-coverage Smartseq2 data.

* This data use the Smartseq2 data from the mouse brain. This data consists of:
   - an expression matrix where each column corresponds to a gene (or transcript) and each row corresponds to a single cell
   - a table of metadata describing each cell
* **This data consists of an expression matrix where each column corresponds to a gene (or transcript) and each row corresponds to a single cell and a table of metadata describing each cell.**


### 0- Single-cell RNA-seq: Introduction & Workflow - [Kaggle Notebook](https://www.kaggle.com/hrishikeshp/0-single-cell-rna-seq-introduction-workflow) 
- Basic theoretical concepts about Bulk RNA-seq and Single-cell RNA-seq
- Single-cell RNA sequencing workflow and Computational analysis

### 1- Exploring AnnData and Preprocessing - [Kaggle Notebook](https://www.kaggle.com/hrishikeshp/1-exploring-anndata-preprocessing) 
- Introduction and theory of AnnData objects
- Exploring a test anndata from SCVI
- Creating an Anndata object from the brain-cells csv files in the dataset
- Preprocessing: Labeling spike-ins

### 2. Quality Control in Single-cell RNA-seq data - [Kaggle Notebook](https://www.kaggle.com/hrishikeshp/2-quality-control-in-single-cell-rna-seq-data) 
- Computing the quality control metrics across cells and genes
- Performed Quality control in cells by removing cells with (i)a low number of reads, (ii)very few unique genes, and (iii)low starting amounts of endogenous RNA
- Quality control in genes by removing "undetectable" genes (A gene is defined to be detectable if at least two cells contain more than 5 reads from the gene)

### 3. Normalization and PCA in scRNA-seq data - [Kaggle Notebook](https://www.kaggle.com/hrishikeshp/3-normalization-and-pca-in-scrna-seq-data) 
- Directly performing PCA on quality controlled data
- Normalizing cell library size using CPM normalization, and then performing PCA
- Normalizing each cell by total counts over all genes, and then performing PCA
- Removing "offending" genes(very highly expressed genes) such as Rn45s, and then performing PCA
- Finally, Normalization by log1p, scaling and then PCA.

The next part of the project involves dimensionality reduction and clustering, to observe and further study clusters in cells of a particular subtissue. Following this, the final part of the project will involve investigation of differential expression of genes in various cell classes.
