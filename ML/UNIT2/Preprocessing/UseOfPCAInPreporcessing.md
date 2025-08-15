

---

## **Principal Component Analysis (PCA) in Preprocessing**

**Definition:**
PCA is a **dimensionality reduction technique** that transforms high-dimensional data into a smaller set of **uncorrelated variables (principal components)** while retaining maximum variance.

---

### **Use of PCA in the Preprocessing Stage**

1. **Dimensionality Reduction**

   * Reduces the number of features before model training.
   * Helps avoid the **curse of dimensionality**.

2. **Noise Reduction**

   * Removes less important components (low variance), improving model robustness.

3. **De-correlation of Features**

   * Converts correlated features into independent principal components.
   * Useful for algorithms assuming feature independence (e.g., Naïve Bayes).

4. **Improved Model Efficiency**

   * Smaller feature set → faster training and prediction.

5. **Visualization of High-Dimensional Data**

   * PCA reduces data to **2D/3D** for better understanding and EDA (Exploratory Data Analysis).

---

### **Example:**

* Dataset: 100 features → PCA reduces to 10 principal components → model trains faster with minimal accuracy loss.

---

### **Diagram:**

```
High-Dimensional Data → PCA Transformation → Reduced Feature Space → ML Model
```

---

**Advantages in Preprocessing:**

* Removes redundant information
* Helps avoid overfitting
* Speeds up learning algorithms

**Limitations:**

* Loses some interpretability of original features
* Scaling is required before PCA

---

✅ **Exam Tip:**
For 5 marks:

* Define PCA (1 mark)
* List 3–4 preprocessing uses (3 marks)
* Add example/diagram (1 mark)

---

