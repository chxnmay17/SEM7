

---

# **Polynomial Time Reducibility**

### **Definition**

* **Polynomial Time Reducibility** (≤p) is a method to compare the complexity of two decision problems (say **A** and **B**).
* A problem **A** is **polynomial-time reducible** to **B** (denoted **A ≤p B**) if:

  * Every instance of **A** can be **transformed into an instance of B** in **polynomial time**.
  * The answer (YES/NO) to **A** is the same as the answer to the transformed instance of **B**.

---

### **Formal Expression**

If there exists a polynomial-time computable function **f** such that:

$$
x \in A \iff f(x) \in B
$$

then **A ≤p B**.

---

### **Importance in Computational Complexity**

1. **Comparing Problem Difficulty**

   * Shows if solving problem **B** also gives a way to solve problem **A** efficiently.

2. **NP-Completeness Proofs**

   * Used to prove problems are **NP-Complete**:

     * If **A ≤p B** and **B** is in P, then **A** is also in P.
     * If **A ≤p B** and **A** is NP-Complete, then **B** is at least as hard as **A**.

3. **Classification of Problems**

   * Helps group problems into **tractable (P)** and **intractable (NP-hard/NP-complete)** categories.

---

### **Real-world Example**

* **3-SAT ≤p CLIQUE**:

  * The Boolean satisfiability problem (3-SAT) can be **reduced** in polynomial time to the CLIQUE problem.
  * Proves CLIQUE is **NP-Complete**.

---

### **Diagram**

```
 Problem A   --poly time reduction-->   Problem B
   (hard)                                  (easier or known class)
```

---

### **Conclusion**

* Polynomial time reducibility is a **fundamental tool in computational complexity theory**.
* It helps in **proving NP-completeness**, **understanding relationships between problems**, and deciding **which problems are computationally feasible**.

---

✅ **Exam Tip Mnemonic**: **"Transform, Compare, Classify"**

* **Transform** → reduce one problem to another.
* **Compare** → relative difficulty.
* **Classify** → P, NP, NP-Complete, NP-Hard.

---

