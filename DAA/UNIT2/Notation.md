
*"What do Ω and Θ notations mean? When do we use O notation?"*

---

## **1. Ω (Omega) Notation – Lower Bound**

* **Meaning**: Describes the **minimum growth rate** of an algorithm’s running time.
* Formal definition:
  $T(n) = \Omega(g(n))$ if ∃ constants $c>0, n_0$ such that

  <img width="230" height="46" alt="image" src="https://github.com/user-attachments/assets/ab141f85-5ea3-4ee6-aba0-8cca41b27b27" />

* **Interpretation**:
  Algorithm will take **at least** proportional to $g(n)$ time for large inputs.
<img width="472" height="86" alt="image" src="https://github.com/user-attachments/assets/25868d93-1043-412f-8504-f81ecea70850" />


---

## **2. Θ (Theta) Notation – Tight Bound**

* **Meaning**: Describes the **exact growth rate** (both upper and lower bounds match).
* Formal definition:
  $T(n) = \Theta(g(n))$ if:

  <img width="410" height="45" alt="image" src="https://github.com/user-attachments/assets/7ce0ec78-9ebe-4db8-9651-3ff6478eecd1" />

* **Interpretation**:
  Algorithm’s running time is **asymptotically equal** to $g(n)$.
<img width="310" height="71" alt="image" src="https://github.com/user-attachments/assets/6e7b00d9-4cd8-42f6-ad18-3d4a00744cfa" />


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


