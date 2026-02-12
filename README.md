# CSE546-data-clustering

# Homework 6 – Unsupervised Learning with PCA, t-SNE, and K-Means

This repository contains my solution for Homework 6 of CSE 546 (Machine Learning).  
The assignment focuses on dimensionality reduction, clustering optimization, and clustering validation using high-dimensional (128-dimensional) data.

---

## Objectives
- Visualize 128-dimensional data using **PCA** and **t-SNE**
- Apply **K-Means clustering** to real data
- Optimize the number of clusters (k = 2–20)
- Evaluate clustering quality using:
  - SSE (Elbow Method)
  - Silhouette analysis
  - Adjusted Rand Index (ARI)
- Compare clustering performance before and after dimensionality reduction

---

## Repository Contents
- **`HW 6 CSE 546.ipynb`** — Full Jupyter Notebook with all code (runs independently)
- **`CSE 546 HW 6.pptx`** — Final presentation summarizing experiments, plots, and results
- **Panopto Recording** — 10-minute walkthrough of code and analysis  
https://louisville.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=11bff226-d91b-4fb1-a2c1-b394005925bb&start=0](https://louisville.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=11bff226-d91b-4fb1-a2c1-b394005925bb&start=0)

---

## Methods & Experiments

### **1. Dimensionality Reduction & Visualization**
- Applied **PCA (2D)** to visualize 128D data  
- Applied **t-SNE (2D)** to compare nonlinear embedding results  
- Compared class separability and structural differences between PCA and t-SNE  

---

### **2. K-Means Clustering on 128D Data**
- Varied number of clusters from **k = 2 to 20**
- Selected optimal k using:
  - **SSE vs. k (Elbow plot)**
  - Silhouette analysis
- Generated silhouette plots for the selected k
- Identified core and boundary samples within clusters
- Computed **Adjusted Rand Index (ARI)**  

**ARI (128D K-Means): 0.77**

---

### **3. PCA (20D) + K-Means**
- Reduced 128D data to **20 dimensions using PCA**
- Reapplied K-Means (k = 2–20)
- Selected optimal k using SSE analysis
- Generated silhouette plots for validation
- Computed Adjusted Rand Index  

**ARI (PCA-20D K-Means): 0.769**

---

## Results & Analysis
- PCA reduction from 128D → 20D preserved nearly all clustering structure  
- ARI decreased only slightly (0.77 → 0.769)  
- Indicates redundancy in the original high-dimensional feature space  
- Silhouette plots supported the selected number of clusters  
- Dimensionality reduction did not significantly degrade clustering performance  

---

## Evaluation Metric: Why ARI?
Because clustering is **unsupervised**, cluster labels are arbitrary and cannot be directly compared using standard accuracy.  

The **Adjusted Rand Index (ARI)**:
- Measures similarity between predicted clusters and ground truth labels  
- Is invariant to label permutations  
- Adjusts for chance  
- Ranges from −1 to 1 (1 = perfect agreement)

---

## Video Presentation
A 10-minute walkthrough including:
- Code demonstration (first portion)
- Explanation of results, plots, and comparisons (second portion)

Panopto link:  
https://louisville.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=11bff226-d91b-4fb1-a2c1-b394005925bb&start=0
