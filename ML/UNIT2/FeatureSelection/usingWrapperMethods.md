

---

## **Wrapper Methods for Feature Selection**

**Definition:**
Wrapper methods evaluate subsets of features by **training and testing a predictive model** for each subset.
The subset that gives the **best model performance** (accuracy, F1-score, etc.) is selected.

**Key Characteristics:**

* Model-dependent
* More accurate than filter methods
* Computationally expensive (requires multiple model trainings)

**General Workflow:**

```
Select Feature Subset → Train Model → Evaluate → Select Best Subset
```

---

## **Types of Wrapper Methods**

### **1. Forward Selection**

* **Process:**

  1. Start with no features.
  2. Add one feature at a time that improves model performance the most.
  3. Stop when no significant improvement.
* **Example:**
  In predicting house prices, start with "Area", then add "Location", then "Rooms".
* **Advantage:** Fewer computations than exhaustive search.
* **Limitation:** May miss optimal subset if initial choices are poor.

---

### **2. Backward Elimination**

* **Process:**

  1. Start with all features.
  2. Remove the least significant feature (smallest contribution to performance).
  3. Repeat until performance worsens or desired number of features is reached.
* **Example:**
  For medical diagnosis, start with 20 tests, remove the least useful ones step-by-step.
* **Advantage:** Considers full set initially.
* **Limitation:** Expensive for very high-dimensional data.

---

### **3. Recursive Feature Elimination (RFE)**

* **Process:**

  1. Train a model (e.g., SVM, Logistic Regression).
  2. Rank features by importance (model coefficients).
  3. Remove the least important feature(s).
  4. Repeat until desired number of features remains.
* **Example:**
  RFE with linear regression to select top predictors of student performance.
* **Advantage:** Uses model’s own feature ranking for selection.
* **Limitation:** Still requires multiple model trainings.

---

## **Diagram: Wrapper Method Flow**

```
Feature Subset → Train Model → Evaluate → Select / Remove Features → Repeat
```

---

### **Advantages**

* Considers feature interactions
* Often yields higher accuracy than filter methods

### **Disadvantages**

* Computationally expensive for large datasets
* Risk of overfitting on small datasets

---

✅ **Exam Tip:**
For 7 marks:

* Define wrapper methods (1 mark)
* List and explain 3 types with steps/examples (5 marks)
* Add diagram (1 mark)

---

