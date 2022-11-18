# Deep learning-based feature selection for single-cell RNA sequencing data analysis

In this work, we explore the utility of various deep learning-based feature selection methods for scRNA-seq data analysis. We sample from Tabula Muris and Tabula Sapiens atlases to create scRNA-seq datasets with a range of data properties and evaluate the performance of traditional and deep learning-based feature selection methods for cell type classification, feature selection reproducibility and diversity, and computational time. Our study provides a reference for future development and application of deep learning-based feature selection methods for single-cell omics data analyses.

<img width=100% src="https://github.com/HaoHuang-USYD/DL_feature_selection/blob/main/img/main.png"/>

## Installation:
DL feature selection for scRNA-seq is developed using PyTorch 1.11.0 and Captum 0.5.0 and requires >=1 GPU to run. We recommend using conda enviroment to install and run the framework. We assume conda is installed. You can use the provided environment or install the environment by yourself accoring to your hardware settings. Note the following installation code snippets were tested on a Windows system (Win10 professional) with NVIDIA GeForce RTX 3090 GPU. The installation process needs about 15 minutes.
 
### Installation using provided environment
Step 1: Create and activate the conda environment for matilda using our provided file
```
conda env create -f environment_DL_feature_selection.yaml
conda activate DL_feature_selection
```

Step 2:
Obtain DL_feature_selection by clonning the github repository:
```
git clone https://github.com/HaoHuang-USYD/DL_feature_selection.git
```

## Preparing intput
The main function takes expression data (i.e. RNA) in `.h5` format and cell type labels in `.csv` format, with log-normalised count data. 
An example for creating .h5 file with Utils/utils.R from a singlecellexperiment object in the R environment is as below:
```
source("utils.R")

# singlecellexperiment object (sce) with cellTypes as cell type annotation
train.exprsmat = as.matrix(logcounts(sce))
write_h5_DL(exprs_list = list(rna = train.exprsmat),
                 h5file_list = c("data.h5")))
write_csv_DL(cellType_list =  list(rna = sce$cellTypes),
               csv_list = c("label.csv")))
```

### Example dataset
Without downloading all the datasets we sampled (see link provided below), one can use the example dataset saved in `Data/Example_dataset`
Training and testing on demo dataset will cost no more than 1 minute with GeForce RTX 3090 GPU.

### edit later: ## Implementation of deep learning-based feature selection methods and notebooks for performing feature selection on sampled datasets are in Utils/Feature_selection_methods/Mlp

## Data sampling for different data characteristics
### Sampled datasets download link:


