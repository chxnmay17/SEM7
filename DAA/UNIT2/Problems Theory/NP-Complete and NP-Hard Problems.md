

---

# **NP-Complete and NP-Hard Problems**

### **1. NP Problems (Non-deterministic Polynomial time)**

* Class of decision problems for which:

  * A solution can be **verified in polynomial time**.
  * May or may not be solvable in polynomial time.

---

### **2. NP-Complete Problems**

* **Definition**:
  A problem is **NP-Complete** if:

  1. It is in **NP** (solution can be verified in polynomial time).
  2. Every NP problem can be **reduced to it in polynomial time**.

* **Importance**:

  * NP-Complete problems are the **“hardest” problems in NP**.
  * If any NP-Complete problem is solved in polynomial time, **P = NP**.

* **Examples**:

  * **SAT (Boolean satisfiability problem)**
  * **3-SAT**
  * **Traveling Salesman Problem (decision version)**
  * **Clique problem**

---

### **3. NP-Hard Problems**

* **Definition**:
  A problem is **NP-Hard** if:

  * Every NP problem can be **reduced to it in polynomial time**.
  * **Not required to be in NP** (solution may not be verifiable in polynomial time).

* **Importance**:

  * NP-Hard problems are **at least as hard as NP-Complete problems**, possibly harder.
  * They include **optimization problems**.

* **Examples**:

  * **Halting Problem** (undecidable)
  * **Optimization version of Traveling Salesman Problem**
  * **Job Scheduling Problem**

---

### **Diagram: Relationship**

```
       NP-Hard
      /       \
  NP-Complete   (harder problems, not in NP)
      |
      NP
      |
      P
```

---

### **Conclusion**

* **NP-Complete** = Hardest problems in NP (decision problems).
* **NP-Hard** = At least as hard as NP, may not be verifiable in polynomial time.
* Understanding these is crucial for classifying **tractable vs. intractable** problems.

---

✅ **Exam Tip Mnemonic:**
**“Complete = Inside NP, Hard = Beyond NP”**

---
