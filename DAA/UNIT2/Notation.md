
*"What do Ω and Θ notations mean? When do we use O notation?"*

---

## **1. Ω (Omega) Notation – Lower Bound**

* **Meaning**: Describes the **minimum growth rate** of an algorithm’s running time.
* Formal definition:
  $T(n) = \Omega(g(n))$ if ∃ constants $c>0, n_0$ such that

  $$
  T(n) \ge c \cdot g(n) \quad \forall n \ge n_0
  $$
* **Interpretation**:
  Algorithm will take **at least** proportional to $g(n)$ time for large inputs.
* **Example**:
  If $T(n) = 3n^2 + 4n$, then $T(n) = \Omega(n^2)$.

---

## **2. Θ (Theta) Notation – Tight Bound**

* **Meaning**: Describes the **exact growth rate** (both upper and lower bounds match).
* Formal definition:
  $T(n) = \Theta(g(n))$ if:

  $$
  c_1 \cdot g(n) \le T(n) \le c_2 \cdot g(n) \quad \forall n \ge n_0
  $$
* **Interpretation**:
  Algorithm’s running time is **asymptotically equal** to $g(n)$.
* **Example**:
  $T(n) = 5n^2 + 3n = \Theta(n^2)$.

---

## **3. When Do We Use O (Big-O) Notation?**

* **Meaning**: Upper bound – worst-case growth rate.
* **Usage in DAA**:

  * To **guarantee performance** in the worst case.
  * To **compare scalability** of algorithms.
  * When only the **upper limit** is known, not the exact growth.
* **Example in Practice**:

  * Searching in a sorted array:

    * Binary search → $O(\log n)$
    * Linear search → $O(n)$
* **Exam Tip**: Most textbooks default to **Big-O** when describing complexity unless tight bounds are required.

---

## **4. Diagram – Growth Bound Comparison**

```
Time ↑
 O (Upper Bound)     ●───────
 Θ (Exact Bound)     ●───────
 Ω (Lower Bound)     ●───────
      +--------------------→ Input Size (n)
```

---

✅ **Key Points for Full Marks**:

* Define **Ω** and **Θ** with **mathematical expressions**.
* Give **simple example** for each.
* Clearly state **Big-O usage cases**.

---


