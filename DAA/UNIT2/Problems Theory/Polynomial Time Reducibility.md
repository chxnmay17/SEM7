

---

# **Polynomial Time Reducibility**

### **Definition**

* **Polynomial Time Reducibility** (≤p) is a method to compare the complexity of two decision problems (say **A** and **B**).
* A problem **A** is **polynomial-time reducible** to **B** (denoted **A ≤p B**) if:

  * Every instance of **A** can be **transformed into an instance of B** in **polynomial time**.
  * The answer (YES/NO) to **A** is the same as the answer to the transformed instance of **B**.

### More Simpler way to define:

> **Polynomial-time reducibility** is when we can **map any input of Problem A to an input of Problem B** in polynomial time, such that solving B gives the correct answer for A.
This transformation must be:

* **Correct**: The YES/NO answer must stay the same.
* **Efficient**: The transformation (using function **f**) must take **polynomial time**.
We write this as:
**A ≤p B**

---

### **Formal Expression**

If there exists a polynomial-time computable function **f** such that:

$$
x \in A \iff f(x) \in B
$$

then **A ≤p B**.

---

### 🧠 **Why Reducibility Matters**

#### 🔁 **Comparing Problem Difficulty**

* If we can reduce **A to B**, and B is easy to solve,
  then **A is also easy**.
* It helps us know which problems are **harder or easier**.

---

#### 🧩 **Used in NP-Completeness Proofs**

* To prove a problem is **NP-Complete**, we use reducibility.
* Example rules:

  * If **A ≤p B** and **B is easy (in P)** → then **A is also easy**.
  * If **A ≤p B** and **A is already NP-Complete** → then **B is at least as hard as A**.

---

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









