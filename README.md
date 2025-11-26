# Final Project: Generative Modeling & Causal Discovery
**STAT433 (Fall 2025)**

## Overview
In this project, you will apply **Score-based Generative Models** or **Flow Matching** to high-dimensional data. The goal is to restore the training data distribution, discover the topological order of the causal graph, and detect Out-of-Distribution (OOD) samples.

## Dataset
* **Unique Data:** Every student will receive a different dataset based on a unique Erdös-Renyi causal graph.
* **Data Format:** > 100-dimensional tabular data.
* **Distribution:** Your specific data (`train_*.npy`, `test_*.npy`) will be sent to your email. Please place them in the `data/` directory.

---

## Problem Descriptions

### (Problem 1; 20pt) Generative Modeling & Data Restoration
* **Task:** Apply **Score-based Generative Model** or **Flow Matching** to restore the training data (> 100-dim).
* **Evaluation:** Evaluate its performance on test data in terms of **MMD (Maximum Mean Discrepancy) score**.
* **Hint:** Please refer to the provided `solver.py` structure.

### (Problem 2; 20pt) Causal Discovery
* **Task:** Determine the **topological order** of the causal graph of the given data.
* **Method:** Evaluate the variance of the score model’s **Jacobian** (Implement **SCORE** or **DiffAN** algorithm).
* **Note:** We will provide an example code demonstrating Jacobian calculation on 2-variable data.

### (Problem 3; 20pt) OOD Detection
* **Task:** Classify the In-Distribution (ID) samples and Out-of-Distribution (OOD) data points.
* **Method:** Use the **Instantaneous Change-of-Variable formula** to calculate likelihood (or negative likelihood).
* **Evaluation:** Classification accuracy based on the threshold you set.

---

## Submission Guidelines
* **File Structure:** You must implement your solution in `src/solver.py`.
* **Requirements:** Please specify the libraries and versions you used in `requirements.txt`.
* **Cheating & Plagiarism:**
    * Code similarity checks will be performed.
    * If plagiarism is detected, **credit will be given to the student who submitted (committed) first.**
    * Please do not share your code.
