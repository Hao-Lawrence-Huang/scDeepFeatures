# Deep learning-based feature selection for single-cell RNA sequencing data analysis

In this work, we explore the utility of various deep learning-based feature selection methods for scRNA-seq data analysis. We sample from Tabula Muris and Tabula Sapiens atlases to create scRNA-seq datasets with a range of data properties and evaluate the performance of traditional and deep learning-based feature selection methods for cell type classification, feature selection reproducibility and diversity, and computational time. Our study provides a reference for future development and application of deep learning-based feature selection methods for single-cell omics data analyses.

<img width=100% src="https://github.com/HaoHuang-USYD/DL_feature_selection/blob/main/img/main.png"/>

## Installation:
DL feature selection for scRNA-seq is developed using PyTorch 1.11.0 and Captum 0.5.0 and requires >=1 GPU to run. We recommend using conda enviroment to install and run the framework. We assume conda is installed. You can use the provided environment or install the environment by yourself accoring to your hardware settings. Note the following installation code snippets were tested on a Windows system (Win10 professional) with NVIDIA GeForce 3090 GPU. The installation process needs about 15 minutes.

## Subsampled data download link:

## Implementation of deep learning-based feature selection methods and notebooks for performing feature selection on sampled datasets are in Utils/Feature_selection_methods/Mlp
