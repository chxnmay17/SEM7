*"Is 6n³ = Θ(n²)? Justify"* 
---

# **Q1)Is 6n³ = Θ(n²)? – Justification**

## **1. Recall Θ-Notation Definition**

* **f(n) = Θ(g(n))** if **∃ positive constants** c₁, c₂, and n₀ such that:

$$
c_1 \cdot g(n) \le f(n) \le c_2 \cdot g(n), \quad \forall n \ge n_0
$$

---

## **2. Given**

* **f(n) = 6n³**
* **g(n) = n²**

---

## **3. Check Upper Bound (O(n²))**

* We test if $6n^3 \le c_2 \cdot n^2$ for large n.
* Dividing by $n^2$:
  $6n \le c_2$ → **Not true** for large n (since n → ∞).
  ✅ **Conclusion**: **6n³ is NOT O(n²)** → cannot be Θ(n²).

---

## **4. Final Conclusion**

* Since Θ-notation requires **both upper and lower bounds**, and **O(n²)** fails:

$$
6n^3 \ne \Theta(n^2)
$$

* **Reason**: n³ grows faster than n²; f(n) is actually **Θ(n³)**.

---

## **5. Diagram – Growth Comparison**

```
Time ↑
      6n³    ●
             |
             |
             |
      n²   ●
             +----------------→ n
```

*(n³ curve grows faster than n²)*

---

✅ **Exam Tip**: Always compare growth rates; higher-degree polynomial terms dominate for large n.

---

---
*"If f(n) = O(g(n)) then does it imply g(n) = O(f(n))? Discuss"* 

---

# **Q2).Does f(n) = O(g(n)) ⇒ g(n) = O(f(n))?**

## **1. Recall Big-O Definition**

* **f(n) = O(g(n))** means:
  There exist constants $c > 0$ and $n_0 > 0$ such that:

  $$
  0 \le f(n) \le c \cdot g(n), \quad \forall n \ge n_0
  $$
* This is a **one-way upper bound** on growth rate.

---

## **2. Question**

* Does $f(n) = O(g(n))$ imply $g(n) = O(f(n))$?
* **Answer**: **No**, not in general.

---

## **3. Counter Example**

Let:

* $f(n) = n$
* $g(n) = n^2$

**Step 1 – Check f(n) = O(g(n)):**

$$
n \le c \cdot n^2 \quad \text{for} \quad n \ge 1, \; c=1
$$

✅ True → $f(n) = O(g(n))$

**Step 2 – Check g(n) = O(f(n)):**

$$
n^2 \le c \cdot n \quad \text{not true for large } n
$$

❌ False

**Conclusion**: The reverse implication does not hold.

---

## **4. When Both Can Hold**

* Both $f(n) = O(g(n))$ and $g(n) = O(f(n))$ hold **only if**:

  $$
  f(n) = \Theta(g(n))
  $$
* This means both functions grow at the **same rate**.

---

## **5. Diagram – Growth Rate**

```
Time ↑
      g(n) = n²   ●
                  |
                  |
      f(n) = n    ●
                  +----------------→ n
```

*(n² grows faster than n, so reverse bound fails)*

---

✅ **Exam Tip**:
Write **definition → answer (No) → counter example → condition for both to hold (Θ)** to score full marks.

---


