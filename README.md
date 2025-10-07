# PCA of Genomic Data — Namib/Angola Project

[![Python](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)]()
[![PLINK](https://img.shields.io/badge/PLINK-v1.9-green.svg)](https://www.cog-genomics.org/plink/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## Project Description

An educational project focused on analyzing genomic data using **Principal Component Analysis (PCA)**.  
The goal is to reproduce and visualize the PCA results from the publication:  
*Oliveira S. et al., Genome-wide variation in the Angolan Namib Desert reveals unique pre-Bantu ancestry, Sci. Adv. 9 (2023)*

---

## Analysis Pipeline

1. **Data Preprocessing (via PLINK)**  
   - SNP filtering  
   - Removing individuals with low call rate  
   - LD pruning  
   - Selecting autosomal SNPs only  

2. **PCA Analysis**  
   - Computing PCs (PC1–PC20)  
   - Explained variance ratios  
   - Visualization: PC1 vs PC2, PC2 vs PC3, etc.  

3. **Visualization & Interpretation**  
   - Coloring samples by population  
   - Overlaying geographical coordinates (synthetic and/or from supplementary materials)  
   - Checking correlations between PCs and coordinates  
   - Clustering in PC space (PyCaret, KMeans, etc.)  

---

## Results

- PCA clusters broadly reflect **geographical population structure**.  
- Clustering confirms separation into groups consistent with ethnic and regional divisions.  
- Some plots (especially maps and interactive visualizations) may render correctly **only inside Jupyter or Colab** environments.

---

## How to Run

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Launch the notebook locally:
   ```bash
   jupyter notebook Practice_PCA_genotypes_final.ipynb
   ```

---

## Tools & Libraries

- Python 3.10+
- PLINK v1.9
- `pandas`, `numpy`, `scikit-learn`
- `matplotlib`, `seaborn`, `plotly`, `folium`
- `pycaret` (for clustering)

---

## ⚠ Note

The dataset was provided as pre-filtered (LD-pruned) as part of the course.  
All major preprocessing steps are still included in the notebook for clarity and reproducibility.
