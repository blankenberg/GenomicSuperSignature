[![Travis-CI Build Status](https://travis-ci.com/shbrief/PCAGenomicSignatures.svg?branch=master)](https://travis-ci.org/shbrief/PCAGenomicSignatures)
[![Coverage Status](https://codecov.io/github/shbrief/PCAGenomicSignatures/coverage.svg?branch=master)](https://codecov.io/github/shbrief/PCAGenomicSignatures?branch=master)
[![R build status](https://github.com/shbrief/PCAGenomicSignatures/workflows/R-CMD-check/badge.svg)](https://github.com/shbrief/PCAGenomicSignatures/actions)


## PCAGenomicSignatures
**Interpretation of RNA-seq experiments through robust, efficient comparison to public databases**

### PURPOSE
Thousands of RNA sequencing profiles have been deposited in public archives, yet 
remain unused for the interpretation of most newly performed experiments. Methods 
for leveraging these public resources have focused on the interpretation of existing 
data, or analysis of new datasets independently, but do not facilitate direct comparison 
of new to existing experiments. The interpretability of common unsupervised analysis 
methods such as Principal Component Analysis would be enhanced by efficient comparison 
of the results to previously published datasets.

### METHODS
To help identify replicable and interpretable axes of variation in any given gene 
expression dataset, we performed principal component analysis (PCA) on 536 studies 
comprising 44,890 RNA sequencing profiles. Sufficiently similar loading vectors, 
when compared across studies, were combined through simple averaging. We annotated 
the collection of resulting average loading vectors, which we call Replicable Axes 
of Variation (RAV), with details from the originating studies and gene set enrichment 
analysis. Functions to match PCA of new datasets to RAVs from existing studies, 
extract interpretable annotations, and provide intuitive visualization, are implemented 
as the PCAGenomicSignatures R package, to be submitted to Bioconductor. 

### Results
Usecases and benchmarking examples are further documented at [PCAGenomicSignaturesPaper](https://shbrief.github.io/PCAGenomicSignaturesPaper/) page.




## Installation
```
devtools::install_github("shbrief/PCAGenomicSignatures")
```

## Schematic
Here is the overview of using PCAGenomicSignatures.
<img src="https://raw.githubusercontent.com/shbrief/PCAGenomicSignatures/master/vignettes/GSig_model_usage_diagram.png"/>

PCAGenomicSignatures allows you to connect your gene expression data to the existing 
database through the expression profile itself. You only need to provide your gene
expression matrix.
<img src="https://raw.githubusercontent.com/shbrief/PCAGenomicSignatures/master/vignettes/GSig_knowledge_network.png"/>

