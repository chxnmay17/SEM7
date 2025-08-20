

---

# Kernel Principal Component Analysis (Kernel PCA)

### Definition

* **Kernel PCA** is an extension of **Principal Component Analysis (PCA)** that allows **non-linear dimensionality reduction**.
* It uses the **kernel trick** to project data into a **higher-dimensional feature space**, where it becomes linearly separable, and then applies PCA.

---

### Why Kernel PCA?

* Standard PCA works only for **linearly separable data**.
* Many real-world datasets (e.g., images, speech, patterns) are **non-linear**.
* Kernel PCA handles this by mapping data into a higher-dimensional space without explicitly computing the mapping.

---

### Working Steps

1. **Mapping:** Input data $x$ is mapped to high-dimensional space using a kernel function $\phi(x)$.
2. **Kernel Trick:** Instead of computing $\phi(x)$, compute dot products using a **kernel function** $K(x_i, x_j)$.

   * Common kernels: Polynomial kernel, Gaussian (RBF) kernel, Sigmoid kernel.
3. **Covariance in Feature Space:** Compute covariance matrix in transformed space using kernel values.
4. **Eigen Decomposition:** Find eigenvalues and eigenvectors of the kernel matrix.
5. **Projection:** Select top eigenvectors → reduced dimensions with **non-linear separability preserved**.

---

### Common Kernel Functions

* **Linear Kernel:** $K(x,y) = x^T y$ (reduces to normal PCA)
* **Polynomial Kernel:** $K(x,y) = (x^T y + c)^d$
* **RBF (Gaussian) Kernel:** $K(x,y) = \exp(-||x-y||^2 / 2\sigma^2)$

---

### Example (Visualization Use-Case)

* **Spiral dataset** or **circular clusters**:

  * PCA fails (linear projection cannot separate).
  * Kernel PCA with **RBF kernel** maps spirals into higher dimensions where they become separable.

---

### Diagram (simple)

```
Original Space (non-linear)       Feature Space (linear after mapping)
   ⭕⭕⭕   ❌❌❌                          ⭕⭕⭕
   ❌❌⭕   ⭕⭕❌       ---> KPCA --->      ❌❌❌  (clearly separable)
```

---

### Advantages

* Captures **non-linear patterns**.
* More powerful than normal PCA for complex datasets.
* Widely used in **image recognition, face recognition, denoising, and anomaly detection**.

---

### Limitation

* Choice of kernel and parameters is critical.
* Computationally expensive for large datasets (kernel matrix grows with $n^2$).

---

✅ **Exam Tip Mnemonic – “MKEPA”**

* **M**ap data to high dimension
* **K**ernel trick
* **E**igen decomposition
* **P**rojection to new features
* **A**pply to non-linear data

---


