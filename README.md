# 🧠 Handwritten Digit Recognition using Classical Machine Learning  
**Virtualyyst AI Assignment Submission**

---

## 📌 Overview

This repository contains my submission for the **Virtualyyst AI Assignment: Handwritten Digit Recognition**.  
The goal of the assignment is to build an end-to-end machine learning pipeline to classify handwritten digit images (0–9) using **classical machine learning techniques**, without using neural networks or pre-trained models.

The implementation is fully contained in a single executed Jupyter notebook and focuses on:
- Understanding image data in tabular (CSV) form
- Implementing and evaluating classical ML models
- Clearly explaining design decisions and limitations

---

## 📂 Dataset

- **Dataset**: MNIST subset in CSV format
- **Structure**:
  - `label` → digit class (0–9)
  - `pixel0` to `pixel783` → flattened 28×28 grayscale image pixels
- Pixel values range from **0 to 255**

---

## 🧪 Workflow Summary

### 1️⃣ Data Loading & Exploration
- Dataset loaded using **Pandas**
- Verified:
  - Dataset shape
  - Class distribution
  - Absence of missing values
- Sample images visualized by reshaping rows into **28×28** matrices

---

### 2️⃣ Preprocessing
- Pixel values normalized to the range **[0, 1]**
- Dataset split into **training and testing sets (80/20)**

---

## 🤖 Model Implementations

### 🔹 K-Nearest Neighbors (KNN) — *From Scratch*
- Implemented **manually without using scikit-learn**
- Euclidean distance–based neighbor search
- Due to high computational cost, evaluation was performed on a **subset of 300 test samples**
- Achieved ~**98% accuracy on this subset**

#### Important Notes:
- This evaluation is **not representative of full test-set performance**
- KNN was tested primarily to **validate correctness of the from-scratch implementation**
- **No confusion matrix was generated** for KNN, as the subset size was intentionally limited

---

### 🔹 Support Vector Machine (SVM)
- Implemented using **scikit-learn**
- **Linear kernel** was used

#### Why Linear SVM?
- The dataset is high-dimensional (784 features)
- RBF kernel would require:
  - Much higher computational cost
  - Dimensionality reduction (e.g., PCA) for feasibility
- Linear SVM provided a strong balance between performance and efficiency

---

### 🔹 Decision Tree
- Implemented using **scikit-learn**
- Tuned parameters such as:
  - `max_depth`
  - `min_samples_split`
- Used to compare interpretability vs generalization performance

---

## 📊 Model Evaluation

- **Accuracy** computed for all evaluated models
- **Confusion matrices generated only for:**
  - Linear SVM
  - Decision Tree
- Confusion matrices visualized using heatmaps
- Misclassified samples were inspected to understand error patterns

---

## 📈 Model Comparison & Analysis

- **Linear SVM** achieved the best overall performance on the full test set
- **Decision Tree** showed reasonable accuracy but signs of overfitting
- **KNN (from scratch)** demonstrated strong performance on a small subset but is computationally impractical at scale

### Observed Misclassifications:
- Visually similar digits (e.g., 4 vs 9, 3 vs 5)
- Variations in handwriting style and stroke thickness

---

## 🧩 Flow Diagram

A **flow diagram** is included in the notebook that outlines:
- Data loading
- Preprocessing
- Model training
- Evaluation steps

<img width="501" height="513" alt="Flow diagram" src="https://github.com/user-attachments/assets/8fa07d9f-7d9f-4992-9cc2-d47aae71e3d4" />

This satisfies the technical execution flow requirement of the assignment.

---

## 🛠 Tools & Libraries Used

- Python  
- NumPy  
- Pandas  
- scikit-learn  
- Matplotlib / Seaborn  

---

## 🚫 Constraints Followed

- ❌ No neural networks  
- ❌ No pre-trained models  
- ❌ No LLMs or managed cloud platforms  
- ✅ Classical ML only  
- ✅ One model implemented from scratch  

---

## 📌 Submission Notes

- All notebook cells are **executed**
- Code includes **inline comments and markdown explanations**
- Outputs, plots, and visualizations are visible
- Explanations reflect **actual implementation decisions and limitations**

---

## 👤 Author

**Rudransh Jaiswal**  
