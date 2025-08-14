

---

## **Best, Worst, and Average Case Behaviour/Analysis of an Algorithm**

**Definition:**
Algorithm analysis evaluates the **running time** (or other resources) as a function of the input size $n$.
The performance may differ for **different inputs of the same size** — hence **best, average, worst case**.
For the same input size $n$, the number of steps executed by an algorithm can differ depending on the **input data arrangement**.
Hence, we analyse **three cases**:

---

### **1. Best Case**

* **Meaning:** Minimum time taken for any input of size $n$.
* **Nature:** **Optimistic** scenario.
* **Use:** Rare in practical guarantees.
* **Example (Linear Search):** Key at **1st position** → 1 comparison → $O(1)$.

```cpp
if(arr[0] == key) return 0; // Best case in O(1)
```

---

### **2. Worst Case**

* **Meaning:** Maximum time taken for any input of size $n$.
* **Nature:** **Pessimistic** scenario.
* **Use:** Ensures **upper bound** performance guarantee.
* **Example (Linear Search):** Key **not present** → $n$ comparisons → $O(n)$.

```cpp
for(i=0; i<n; i++) if(arr[i]==key) return i; // Not found → O(n)
```

---

### **3. Average Case**

* **Meaning:** Expected running time over **all possible inputs**, assuming a probability distribution.
* **Nature:** **Realistic** measure of performance.
* **Formula:**

$$
T_{\text{avg}}(n) = \sum_{i} P(I_i) \cdot T(I_i)
$$
where $P(I_i)$ = probability of $i$-th input.

* **Example (Linear Search):** If element is equally likely at any position or absent:

  * Average comparisons = $(n+1)/2$
  * Complexity: $O(n)$.

---

### **Is Average Case an Average of Best and Worst Cases?**

**No.**

* **Reason:** Best and worst cases are **extreme single scenarios**, while average case considers **all possible inputs** and their **probabilities**.
* Taking $\frac{\text{Best} + \text{Worst}}{2}$ ignores:

  * Distribution of inputs
  * Different probabilities for different inputs
* **Example:**

  * **Best case:** 1 comparison, **Worst case:** 100 comparisons
  * If 90% of inputs take 50 comparisons, average ≠ (1+100)/2 = 50.5.
  * Real average ≈ 50 (weighted by probability).

---

### **Comparison Table**

| Case    | Input Condition                | Purpose           | Example (Linear Search) | Complexity |
| ------- | ------------------------------ | ----------------- | ----------------------- | ---------- |
| Best    | Most favorable                 | Optimistic bound  | Key at 1st position     | $O(1)$     |
| Average | Random input, prob. considered | Realistic measure | Key in middle (avg pos) | $O(n)$     |
| Worst   | Least favorable                | Guaranteed bound  | Key absent              | $O(n)$     |

---

### **Diagram:** Execution Time vs Input Size $n$

```
Time ↑
     |           Worst Case
     |        /
     |   Average Case
     |  /
     | /
     |/ Best Case
     +----------------→ n
```

---

**Key Exam Points to Justify:**

* Best and worst cases are **bounds**; average case is **expected value**.
* **Average ≠ midpoint** — it’s a **probability-weighted mean**.
* Always specify **assumptions about input distribution** in average case analysis.

---


