# Spatial_Transcriptomics
# Introduction

Spatial transcriptomics is a powerful technology that allows researchers to analyze gene expression while preserving spatial context within tissues. This project demonstrates the analysis of spatial transcriptomics datasets generated using 10x Genomics platforms, including Visium (H&E and fluorescence imaging) and Xenium.

The analysis is performed using Python-based tools to explore spatial gene expression patterns, identify clusters, and visualize tissue organization.

# Objectives
Perform preprocessing and quality control of spatial data
Identify highly variable genes
Apply dimensionality reduction techniques
Perform clustering of spatial spots
Visualize gene expression in spatial context
Compare different spatial technologies (Visium vs Xenium)
# Tools and Libraries

The following tools were used:

Scanpy
Squidpy
Matplotlib
NumPy
Pandas
Methodology
Data Loading

Each dataset (Visium and Xenium) is loaded into an AnnData object containing gene expression values and spatial coordinates.

# Quality Control

Metrics such as total counts and number of genes per spot are calculated. Low-quality spots are removed to improve data reliability.

# Normalization

Data is normalized to correct for sequencing depth differences and log-transformed for stability.

# Highly Variable Genes

The most informative genes are selected to improve downstream analysis.

# Dimensionality Reduction

Principal Component Analysis (PCA) is used to reduce dimensionality while preserving important variance.

# Clustering

Leiden clustering algorithm groups spots into clusters representing distinct biological regions.

# UMAP Visualization

UMAP is used to visualize clusters in a two-dimensional space.

# Spatial Visualization

Clusters and gene expression are mapped onto tissue images (H&E or fluorescence).

# Spatial Analysis

Spatial relationships between clusters are analyzed using neighborhood enrichment and spatial autocorrelation.

# Results

The analysis generates the following outputs:

Quality control violin plots
Highly variable gene selection plots
PCA variance plots
UMAP visualizations
Cluster identification plots
Spatial tissue maps (H&E and fluorescence)
Marker gene identification
Spatial interaction heatmaps

These outputs help in understanding tissue architecture and gene expression patterns.

# Visium vs Xenium
Feature	Visium	Xenium
Resolution	Spot-level	Single-cell / subcellular
Imaging	H&E / Fluorescence	High-resolution imaging
Data Type	Bulk per spot	Single molecule detection
How to Run

Install required libraries:

pip install scanpy squidpy matplotlib seaborn
Open notebooks:
Visium H&E analysis
Visium fluorescence analysis
Xenium analysis
Run all cells step by step
# Conclusion

This project demonstrates how spatial transcriptomics data can be analyzed using Python tools. By integrating gene expression with spatial information, we can better understand tissue structure and biological processes. The comparison between Visium and Xenium highlights differences in resolution and analytical capabilities.

# Future Work
Cell type annotation
Integration with single-cell RNA-seq
Advanced spatial modeling
Cross-sample comparison
