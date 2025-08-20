

---

# Principal Component Analysis (PCA) – Process

### Definition

* **PCA** is a **dimensionality reduction technique** used in Machine Learning.
* It transforms high-dimensional data into a **smaller set of uncorrelated variables (Principal Components)** while preserving maximum variance (information).

---

### **Steps in PCA Process**

1. **Standardize the Data**

   * Scale features so they have mean = 0 and variance = 1.
   * Ensures fair comparison when features are measured in different units.

2. **Compute Covariance Matrix**

   * Measures how variables vary together.
   * $\text{Cov}(X,Y) > 0$ → variables increase together,
     $\text{Cov}(X,Y) < 0$ → one increases, other decreases.

3. **Calculate Eigenvalues & Eigenvectors**

   * **Eigenvectors** → direction of new feature axes (Principal Components).
   * **Eigenvalues** → amount of variance captured by each eigenvector.

4. **Select Principal Components**

   * Sort eigenvalues (largest → smallest).
   * Choose top *k* components capturing most variance (e.g., 95%).

5. **Form New Feature Space**

   * Project original data onto selected eigenvectors.
   * This gives a reduced dataset with fewer dimensions.

---

### **Diagram (Conceptual Flow)**

```
 Original Data → Standardization → Covariance Matrix → 
 Eigen Decomposition → Select Top k Components → Reduced Data
```

---

### **Example (Real-world)**

* **Face Recognition (Eigenfaces):**
  Instead of using every pixel (high-dimensional), PCA reduces to few principal components (eigenfaces) capturing essential features → faster recognition.

---

### **Advantages of PCA**

* Reduces dimensionality → less computation.
* Removes redundancy (correlated features).
* Improves visualization in 2D/3D.

---

✅ **Exam Mnemonic – S.C.E.S.F.** (Steps of PCA)

* **S**tandardize data
* **C**ovariance matrix
* **E**igen decomposition
* **S**elect principal components
* **F**orm new dataset

---


