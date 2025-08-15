

---

## **Q: Explain Geometric and Probabilistic Models with Suitable Examples**

---

### **1. Geometric Model**

#### **Definition**

* ML approach where data points are represented in a **geometric space** (often high-dimensional), and predictions are made using **geometric relationships** like **distance, angles, or hyperplanes**.
* Decision boundaries are created **geometrically** to separate classes.

#### **Key Points**

* Works on **vector space representation** of data.
* Relies on **distance metrics** (e.g., Euclidean, Manhattan, Cosine).
* Classification/decision made by **position** of data points relative to boundaries.

#### **Examples**

* **k-Nearest Neighbors (k-NN)** → Assigns class based on closest neighbors in space.
* **Support Vector Machines (SVM)** → Finds optimal hyperplane separating classes.
* **Clustering algorithms** like k-Means.

#### **Advantages**

* Intuitive, visual interpretation.
* Effective when classes are geometrically separable.

#### **Limitations**

* Struggles with non-linearly separable data (unless transformed).

---

### **2. Probabilistic Model**

#### **Definition**

* ML approach based on **probability theory**; models the **likelihood** that a data point belongs to a particular class.
* Predictions are made by **computing and comparing probabilities**.

#### **Key Points**

* Learns **probability distribution** of features given classes or vice versa.
* Often uses **Bayes’ Theorem** for decision making.
* Can handle **uncertainty** and overlapping classes.

#### **Examples**

* **Naïve Bayes Classifier** → Assumes feature independence; uses Bayes’ Theorem.
* **Hidden Markov Models (HMM)** → Models sequences probabilistically.
* **Gaussian Mixture Models (GMM)** → Represents data as a mixture of Gaussian distributions.

#### **Advantages**

* Handles uncertainty well.
* Works well with small datasets.
* Can model overlapping class regions.

#### **Limitations**

* Requires correct probability assumptions.
* Performance drops if independence/distribution assumptions are wrong.

---

### **3. Comparison Table**

| Feature              | Geometric Model                     | Probabilistic Model                      |
| -------------------- | ----------------------------------- | ---------------------------------------- |
| Basis                | Geometry (distance, angles)         | Probability theory                       |
| Representation       | Data as points/vectors in space     | Data as probability distributions        |
| Decision Criterion   | Nearest neighbor / separating plane | Maximum probability (MAP, ML estimation) |
| Example Algorithms   | k-NN, SVM, k-Means                  | Naïve Bayes, HMM, GMM                    |
| Handling Uncertainty | Poor                                | Good                                     |

---

### **4. Diagram**

```
Geometric Model:
   (Class A)   ○ ○ ○
               │Decision Boundary
   (Class B)   ● ● ●

Probabilistic Model:
   P(Class A|x) = 0.7
   P(Class B|x) = 0.3
   → Predict Class A
```

---

### **5. Real-World Analogy**

* **Geometric Model:** Classifying houses by their **location on a map** (distance-based).
* **Probabilistic Model:** Classifying houses by **chance of being in a flood zone** based on historical probability.

---

✅ **Exam Tip:**
For **7 marks** – write **definitions (2M)**, **examples with key points (3M)**, and **comparison table + diagram (2M)** to score full marks.

---
