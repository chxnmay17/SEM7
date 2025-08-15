

---

## **Statistical Methods to Describe the Nature of Data**

**Definition:**
Statistical methods are used to summarize, understand, and interpret the **distribution, central tendency, spread, and shape** of data before applying ML models.
This is part of **Exploratory Data Analysis (EDA)**.

---

### **1. Measures of Central Tendency**

Describe the **center** of data.

* **Mean (Average):**

  $$
  \text{Mean} = \frac{\sum_{i=1}^n x_i}{n}
  $$

  * Example: Average salary in a company.
* **Median:** Middle value when data is sorted (robust to outliers).
* **Mode:** Most frequently occurring value.

---

### **2. Measures of Dispersion (Spread)**

Describe **variability** in the data.

* **Range:** Max – Min value.
* **Variance:**

 <img width="201" height="73" alt="image" src="https://github.com/user-attachments/assets/514ad841-67be-4d60-8ac8-aa11ab3250f1" />

* **Standard Deviation (SD):** Square root of variance; shows average deviation from mean.
* **Interquartile Range (IQR):** Spread of middle 50% (Q3 – Q1).

---

### **3. Measures of Shape**

Describe **distribution pattern**.

* **Skewness:**

  * Positive skew → tail to right
  * Negative skew → tail to left
* **Kurtosis:**

  * High kurtosis → sharp peak
  * Low kurtosis → flat peak

---

### **4. Frequency Distribution & Visualization**

Summarizes data occurrence.

* **Tables:** Frequency tables
* **Graphs:** Histogram, Bar chart, Pie chart
* **Example:** Histogram of exam scores to see distribution shape.

---

### **5. Correlation Analysis**

Shows **relationship strength** between two variables.

* **Pearson’s correlation coefficient (r):**

 <img width="317" height="89" alt="image" src="https://github.com/user-attachments/assets/140d2ef2-782b-4b4f-9c75-619e740f1562" />


  * $r$ close to 1 → strong positive relation
  * $r$ close to -1 → strong negative relation

---

### **6. Cross Tabulation (for Categorical Data)**

* Compares two categorical variables in a table format.
* Example: Gender vs. Purchase Decision.

---

### **Diagram:**

```
Data → Central Tendency → Dispersion → Shape → Relationship → Visualization
```

---

✅ **Exam Tip:**
For 7 marks:

* Start with definition (1 mark)
* Cover **central tendency, dispersion, shape, correlation, visualization** (5 marks)
* Add example/diagram (1 mark)

---


