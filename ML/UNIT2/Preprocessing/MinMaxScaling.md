

---

## **Min–Max Scaling**

**Definition:**
Min–Max Scaling (also called **Normalization**) is a feature scaling technique that transforms data values to a **fixed range**, usually **\[0, 1]** (or sometimes \[-1, 1]).

**Purpose in ML:**

* Ensures all features contribute equally to the model
* Avoids bias toward features with large numeric ranges
* Improves convergence speed in algorithms like **Gradient Descent, k-NN, SVM, Neural Networks**

---

### **Formula:**

$$
X' = \frac{X - X_{\min}}{X_{\max} - X_{\min}}
$$

Where:

* $X$ = original value
* $X_{\min}$ = minimum value of feature
* $X_{\max}$ = maximum value of feature
* $X'$ = scaled value

---

### **Example:**

Original data (Feature: Age) → **\[20, 25, 30, 50]**

* $X_{\min} = 20$, $X_{\max} = 50$

Scaling for Age = 30:

$$
X' = \frac{30 - 20}{50 - 20} = \frac{10}{30} = 0.333
$$

**Scaled Data:**

| Age (Original) | Age (Scaled) |
| -------------- | ------------ |
| 20             | 0.00         |
| 25             | 0.17         |
| 30             | 0.33         |
| 50             | 1.00         |

---

### **Diagram:**

```
Original Range [20–50] → Min–Max Scaling → New Range [0–1]
```

---

**Advantages:**

* Preserves the original data distribution (no distortion in shape)
* Simple to implement

**Limitations:**

* Sensitive to outliers (extreme values affect scaling)

---

✅ **Exam Tip:**
For a 5-mark answer:

* Definition & purpose (1 mark)
* Formula (1 mark)
* Example with calculation (2 marks)
* Advantage/limitation or diagram (1 mark)

---

