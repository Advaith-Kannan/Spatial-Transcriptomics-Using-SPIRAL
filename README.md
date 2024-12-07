
# README

## Spatial Transcriptomics Using SPIRAL

This repository contains the implementation of SPIRAL for spatially resolved transcriptomics (SRT) datasets. SPIRAL is a novel algorithm for efficient spatial domain identification. The code is designed to process and analyze two datasets: MERFISH and OSMFISH.

### **Datasets**

#### 1. **MERFISH: Mouse Brain Preoptic Hypothalamus Region**
- **Description**: This dataset uses the multiplexed error-robust fluorescence in situ hybridization (MERFISH) technique. It provides a high-resolution view of the preoptic hypothalamus region of the mouse brain.
- **Data Format**: The dataset is stored in an `h5ad` file containing:
  - A spot-gene matrix with gene expression values for each spatial spot.
  - Spatial coordinates (x, y) for the corresponding spots.

#### 2. **OSMFISH: Mouse Brain Somatosensory Cortex Region**
- **Description**: Acquired using the Oligonucleotide Sequential Fluorescence In Situ Hybridization (OSMFISH) technique, this dataset represents the somatosensory cortex region of the mouse brain.
- **Data Format**: Similar to MERFISH, it is stored in an `h5ad` file with:
  - A spot-gene matrix.
  - Spatial coordinates (x, y).

#### Both datasets are available in the following drive folder: [link](https://drive.google.com/drive/folders/1GllYHqgeRihs9-rzl1aPSl-uXwyWH4tm?usp=sharing)
---

### **SPIRAL**

#### **Overview**
SPIRAL (Spatially-aware Integration and Removal of Artifacts in Local domains) is a computational method designed to overcome challenges in analyzing spatial transcriptomics data, such as batch effects and coordinate misalignments. It aims to integrate multiple datasets while preserving spatial domain continuity.

#### **Key Features**
1. **Batch Effect Removal**: SPIRAL effectively normalizes datasets to minimize variations caused by experimental conditions.
2. **Spatial Coordinate Alignment**: Ensures spatial consistency across datasets with differing resolutions or coordinate systems.
3. **Generalization**: Demonstrates strong performance on unseen datasets while maintaining spatial coherence.

#### **Performance**
In this project, SPIRAL was applied to both MERFISH and OSMFISH datasets. Its robustness in spatial domain preservation can be observed based on the clusters formed on both of these datasets. 

---

### **Repository Structure**
All files are provided in `Files/`
- `Dataset1.ipynb`, `Dataset2.ipynb` : Jupyter notebooks for preprocessing, analysis, and visualization. Clustering steps are included in the Rmd files. 
- `Dataset1.py`, `dataset2.py`: Python scripts to reproduce clustering results and generate required outputs.
- `R-File-DS1.Rmd`, `R-File-DS2.Rmd`: Since SPIRAL requires clustering steps to be performed on R, these are provided here as well. 

### **Getting Started**
#### **Prerequisites**
- Python 3.8+
- Required Python libraries specified in `requirements.txt`

#### **Run Instructions**
1. Preprocess datasets using the provided preprocessing notebook.
2. Execute the SPIRAL pipeline to generate clustering results. This will require the usage of the provided rmd files too. 
3. Visualize spatial feature plots using the visualization scripts.
