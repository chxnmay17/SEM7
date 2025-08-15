
---

## **Q: Explain Parametric and Non-Parametric Machine Learning Models**

---

### **1. Parametric Models**

#### **Definition**

* ML models that **assume a fixed functional form** and have a **fixed number of parameters**.
* Learning involves **estimating these parameters** from training data.
* Once parameters are learned, the model cannot increase its complexity, even with more data.

#### **Key Points**

* **Assumption:** Data follows a specific distribution (e.g., linear, Gaussian).
* **Fixed Complexity:** Complexity depends on number of parameters, not on dataset size.
* **Training:** Fast, requires less data.
* **Limitation:** Poor performance if real data doesn’t match assumed form.

#### **Examples**

* Linear Regression
* Logistic Regression
* Naïve Bayes
* Perceptron

#### **Advantages**

* Simpler, faster training.
* Needs less data.
* Easier to interpret.

#### **Disadvantages**

* Strong assumption about data shape.
* Cannot adapt well to complex patterns.

---

### **2. Non-Parametric Models**

#### **Definition**

* ML models that **do not assume a fixed functional form**.
* Model complexity **grows with data size** — more data = better resolution.
* Learns patterns directly from data without strict assumptions.

#### **Key Points**

* **Flexibility:** Can adapt to any distribution.
* **Complexity:** Can increase with more data.
* **Training:** Slower, needs more data.
* **Limitation:** Risk of overfitting.

#### **Examples**

* k-Nearest Neighbors (k-NN)
* Decision Trees
* Support Vector Machines (SVM with RBF kernel)
* Neural Networks (deep models often treated as non-parametric in practice)

#### **Advantages**

* Flexible, no strong distribution assumption.
* Can capture complex patterns.

#### **Disadvantages**

* More computationally expensive.
* Requires more data.
* May overfit if not regularized.

---

### **3. Comparison Table**

| Feature            | Parametric                              | Non-Parametric                  |
| ------------------ | --------------------------------------- | ------------------------------- |
| Assumption on data | Fixed form (e.g., linear)               | No fixed form                   |
| Parameters         | Fixed number                            | Grow with data                  |
| Flexibility        | Low                                     | High                            |
| Training speed     | Fast                                    | Slow                            |
| Data requirement   | Less                                    | More                            |
| Risk               | Underfitting if assumption is wrong     | Overfitting if too complex      |
| Examples           | Linear/Logistic Regression, Naïve Bayes | k-NN, Decision Trees, SVM (RBF) |

---

### **4. Diagram**

```
Parametric: Fixed Shape → Fit Parameters → Predict
Example: Linear Regression (y = mx + c)

Non-Parametric: No Fixed Shape → Learn from Data Points → Predict
Example: k-NN (Prediction based on nearest neighbors)
```

---

### **5. Real-world Analogy**

* **Parametric:** Like fitting clothes from a fixed-size store (S, M, L) — quick but may not fit perfectly.
* **Non-Parametric:** Like tailoring clothes — fits perfectly but takes more time and effort.

---

✅ **Exam Tip:** For 7 marks – write **definition (2M)**, **features & examples (3M)**, and **comparison table + diagram/analogy (2M)** for full score.

---


