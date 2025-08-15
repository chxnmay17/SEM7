
---

## **Q: Explain Geometric Model and Its Types**

---

### **1. Definition**

* **Geometric Model** in Machine Learning is an approach where **data points are represented in a geometric space** (often high-dimensional), and predictions are made based on **geometric relationships** like **distances, angles, or hyperplanes**.
* Goal: Find **decision boundaries** that separate different classes based on their **spatial distribution**.

---

### **2. Key Characteristics**

* Represents data as **vectors** in feature space.
* Relies on **distance metrics** (Euclidean, Manhattan, Cosine similarity).
* Decision is based on **relative position** of data points.
* Works well when data is **geometrically separable**.

---

### **3. Types of Geometric Models**

#### **A. Distance-Based Models**

* **Idea:** Classify based on closeness to known data points.
* **Method:** Compute distance between input point and training data points.
* **Example Algorithms:**

  * **k-Nearest Neighbors (k-NN)** – Class of a point is determined by majority vote of its k closest neighbors.
  * **k-Means Clustering** – Groups points into clusters based on minimum distance to cluster centers.
* **Distance Measures:**

  * Euclidean Distance
  * Manhattan Distance
  * Cosine Similarity

---

#### **B. Linear Classifiers**

* **Idea:** Use a straight line (2D), plane (3D), or hyperplane (nD) to separate classes.
* **Method:** Learn a separating boundary that maximizes separation between classes.
* **Example Algorithms:**

  * **Perceptron** – Simple linear classifier.
  * **Support Vector Machine (SVM)** – Finds the optimal hyperplane that maximizes margin between classes.
* **Decision Boundary:** Linear function in feature space.

---

#### **C. Margin-Based Models**

* **Idea:** Not only separate classes but also maximize the distance (margin) from the nearest points.
* **Example:**

  * **Hard Margin SVM** – Perfectly separates classes with maximum margin.
  * **Soft Margin SVM** – Allows some misclassification for noisy data.

---

### **4. Advantages**

* Intuitive and visually interpretable (especially in low dimensions).
* Effective for data with **clear geometric separation**.
* Works well with small to medium datasets.

---

### **5. Limitations**

* Performance drops with **non-linear boundaries** (unless transformed using kernels).
* High-dimensional spaces may cause **curse of dimensionality**.

---

### **6. Diagram**

```
Distance-Based:
   ● ● ● ○ ○ ○
   Class A  Class B
   (Nearest neighbor determines class)

Linear Classifier:
   ● ● ● | ○ ○ ○
   (Straight line as decision boundary)
```

---

### **7. Real-World Example**

* **Distance-Based:** Grouping news articles by similarity in word usage (cosine similarity).
* **Linear Classifier:** Email spam filtering using SVM to separate spam vs non-spam in feature space.

---

✅ **Exam Tip:**
For **7 marks** – give **definition (1M)**, **types with explanation + examples (4M)**, and **diagram + real-world example (2M)** to ensure full score.

---

