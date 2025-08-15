

---

## **Handling Missing Values in Machine Learning**

**Definition:**
Missing values occur when **no data is stored for a variable** in an observation.
If not handled, they can cause **bias, reduced accuracy, or inability to train models**.

---

### **1. Identify Missing Values**

* **Techniques:**

  * Use `isnull()` / `isna()` in Pandas.
  * Visualize with heatmaps (e.g., Seaborn).
* **Example Table:**

| ID | Age | Salary |
| -- | --- | ------ |
| 1  | 25  | 50000  |
| 2  | NaN | 45000  |
| 3  | 30  | NaN    |

---

### **2. Causes of Missing Values**

* Data entry errors
* Sensor failures
* Incomplete surveys
* Data merging issues

---

### **3. Methods to Handle Missing Values**

#### **A. Deletion Methods**

1. **Listwise Deletion**

   * Remove rows with any missing value.
   * **Pros:** Simple.
   * **Cons:** Data loss.
   * Use when **missing < 5%** of data.
2. **Column Deletion**

   * Remove feature if most values are missing.
   * Example: 95% null column.

---

#### **B. Imputation Methods**

1. **Mean/Median/Mode Imputation**

   * Replace missing value with feature mean (numeric), median, or mode (categorical).
   * **Example:** Salary NaN → replace with average salary.
   * Median is preferred if data has outliers.
2. **Constant Value Imputation**

   * Replace with fixed value (e.g., `0`, `"Unknown"`).
3. **Forward/Backward Fill** (Time-series)

   * Fill using previous (forward) or next (backward) value.
4. **KNN Imputation**

   * Fill using the mean of the k-nearest neighbors’ values.
5. **Regression Imputation**

   * Predict missing values using other features.

---

#### **C. Advanced Approaches**

* **Multiple Imputation (MICE)** – Iteratively predicts missing values.
* **Model-based Handling** – Some models (e.g., XGBoost) handle missing values internally.

---

### **4. Choosing the Right Method**

| Missing Data % | Recommended Method                  |
| -------------- | ----------------------------------- |
| <5%            | Deletion or simple imputation       |
| 5–30%          | Statistical/ML imputation           |
| >30%           | Advanced imputation or drop feature |

---

### **5. Workflow Diagram**

```
Identify Missing Data → Analyze Pattern → Choose Method → Apply → Validate
```

---

### **Real-world Example**

In a **loan approval dataset**, if `Income` has 2% missing values → fill with median income;
if `Credit History` has 80% missing → drop the column.

---

✅ **Exam Tip:**
Mention **identification → methods → when to use → example**.
If time allows, draw the workflow diagram — quick marks booster.

---

