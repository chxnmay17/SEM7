

---

## **Feature Selection**

**Definition:**
Feature selection is the process of selecting a **subset of relevant features** from the original dataset to improve **model performance, reduce overfitting, and lower computational cost**.

**Goals:**

* Remove irrelevant/redundant features
* Improve accuracy & training speed
* Enhance model interpretability

**Benefits:**

* Reduces dimensionality → faster training
* Minimizes overfitting risk
* Improves generalization

---

## **Filtering Techniques for Feature Selection**

Filtering methods evaluate features **independently** of the ML algorithm, using statistical measures.

**Key Characteristics:**

* Fast, simple, and scalable
* Uses statistical scores/rankings
* No model training required for evaluation

---

### **1. Variance Threshold**

* **Idea:** Remove features with low variance (little or no change across samples).
* **Example:** If all values in a feature are `1`, it provides no information.
* **Formula:**

  $$
  \text{Variance} = \frac{\sum (x_i - \bar{x})^2}{n}
  $$
* **Use case:** Preprocessing high-dimensional data.

---

### **2. Correlation Coefficient**

* **Idea:** Remove features highly correlated with each other or target (redundant information).
* **Pearson Correlation Formula:**

 <img width="336" height="79" alt="image" src="https://github.com/user-attachments/assets/035a5d24-fd31-4a44-a75c-186f7a05e18f" />

* **Rule:** Drop one feature if correlation > threshold (e.g., 0.9).
* **Example:** "Height in cm" and "Height in inches" — redundant.

---

### **3. Chi-Square Test (χ²)**

* **Idea:** Measures independence between categorical feature and target variable.
* **Formula:**

  <img width="248" height="80" alt="image" src="https://github.com/user-attachments/assets/3d3a6b81-4236-4e2e-b029-ea6811212f05" />


  where **O** = observed frequency, **E** = expected frequency.
* **Use case:** Feature selection in classification with categorical features.
* **Example:** Selecting keywords for spam classification.

---

### **4. Mutual Information**

* **Idea:** Measures how much information a feature provides about the target variable.
* **Range:** 0 (no info) → higher value (more dependency).
* **Example:** In a movie recommendation system, "User's favorite genre" has high MI with "Watched movie" label.

---

### **5. ANOVA F-test**

* **Idea:** Checks if feature means differ significantly between classes (numerical features, categorical target).
* **Formula (F-statistic):**

  <img width="339" height="69" alt="image" src="https://github.com/user-attachments/assets/01abd21a-7e31-4250-9f67-d25ddbfe7298" />

* **Use case:** Medical data where lab values differ between disease groups.

---

### **Diagram: Filtering Method Workflow**

```
Dataset → Calculate Statistical Score for Each Feature → Rank Features → Select Top-k → Train Model
```

---

### **Advantages of Filtering Methods**

* Fast, simple, works with any model
* Good for high-dimensional datasets (e.g., text data)

### **Limitations**

* Ignores feature interaction
* Might discard features that become useful only in combination

---

✅ **Exam Tip:**
For full marks:

1. Define Feature Selection
2. Define Filtering Techniques
3. Explain **at least 3 methods** with formulas/examples
4. Draw the workflow diagram

---

