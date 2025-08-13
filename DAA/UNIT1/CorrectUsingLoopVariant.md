
# **Algorithm Correctness & Loop Invariant Property**

## **1. Importance of Algorithm Correctness**

* **Definition**: An algorithm is **correct** if, for every valid input, it **terminates** and produces the **expected output**.
* **Why important?**

  1. **Reliability** – Incorrect algorithms may produce wrong results even if they are fast.
  2. **Foundation for Optimization** – Before improving efficiency, we must ensure the algorithm works.
  3. **Avoids Costly Failures** – Errors in algorithms can cause **system crashes**, financial losses, or security breaches.
  4. **Theoretical Guarantee** – In DAA, correctness ensures **proof of validity** using mathematical reasoning.

💡 *Example*:

* A sorting algorithm that is fast but sometimes produces unsorted output is **useless** in practice.

---

## **2. Loop Invariant Property**

* **Definition**:
  A **loop invariant** is a condition that:

  1. Holds **true before** the loop starts.
  2. Remains **true after each iteration** of the loop.
  3. Helps in proving **algorithm correctness**.

* **Purpose in Correctness Proof**:

  * Shows that the algorithm maintains a **valid state** throughout execution.
  * If the invariant is true before and after the loop, and termination gives the desired result → algorithm is correct.

---

## **3. Proving Algorithm Correctness using Loop Invariant**

* **Steps to prove correctness**:

  1. **Initialization** – Show invariant holds before first iteration.
  2. **Maintenance** – Show invariant remains true after each iteration.
  3. **Termination** – When loop ends, invariant + loop condition ⇒ correctness.

---

## **4. Example: Summation of first *n* numbers**

### **Algorithm**

```c
sum = 0;
for (i = 1; i <= n; i++) {
    sum = sum + i;
}
```

---

### **Loop Invariant Property**

> At the start of each iteration of the loop,
> **sum = 1 + 2 + ... + (i - 1)**.

---

### **Proof**

1. **Initialization**

   * Before first iteration: `i = 1`, `sum = 0`.
   * Invariant: sum of numbers from 1 to (i−1) = sum of 1 to 0 = 0 ✅.

2. **Maintenance**

   * Assume invariant holds for iteration `k`:
     `sum = 1 + 2 + ... + (k - 1)`.
   * In iteration `k`:
     `sum = sum + k` ⇒ `sum = 1 + 2 + ... + k`.
   * At start of next iteration `(k+1)`, invariant holds again ✅.

3. **Termination**

   * Loop stops when `i = n + 1`.
   * Invariant: `sum = 1 + 2 + ... + n` → **Correct result**.

---

### **Diagram (State Progression)**

```
i   sum (before iteration)   sum (after iteration)
1   0                        1
2   1                        3
3   3                        6
... ...                      ...
n   sum till n-1              sum till n
```

---

✅ **Conclusion**: Since the invariant holds for **Initialization**, **Maintenance**, and **Termination**, the algorithm is **correct**.

---

## **5. Exam Quick Mnemonic**

**I-M-T** = **Initialization – Maintenance – Termination** → proves correctness via loop invariant.

---

