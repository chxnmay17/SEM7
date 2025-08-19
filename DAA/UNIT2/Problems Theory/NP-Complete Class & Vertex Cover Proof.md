

---

# NP-Complete Class & Vertex Cover Proof

## 1) **NP-Complete Class Problems**

* **Definition**: A problem is **NP-Complete** if:

  1. It belongs to **NP** (solution can be verified in polynomial time).
  2. Every problem in NP can be **polynomial-time reduced** to it.

* **Significance**:

  * Central to **P vs NP** question.
  * If any NP-Complete problem is solved in polynomial time → **all NP problems are solvable in polynomial time**.

---

## 2) **Vertex Cover Problem**

* **Definition**: Given a graph $G=(V,E)$ and integer $k$, is there a subset of vertices $V' \subseteq V$ such that:

  * $|V'| \leq k$
  * Every edge in $E$ has at least one endpoint in $V'$.
* **Decision Problem**: “Does a vertex cover of size ≤ $k$ exist?”

---

## 3) **Steps to Prove Vertex Cover is NP-Complete**

### (A) **Vertex Cover ∈ NP**

* Given a set of vertices, we can check in polynomial time if all edges are covered → hence **verification is polynomial**.

---

### (B) **Reduction from 3-SAT / CLIQUE**

* Standard reduction is from **CLIQUE problem** (already NP-Complete).

* **Reduction Idea**:

  * Clique in $G$ ↔ Vertex Cover in complement graph $G'$.
  * If graph $G$ has a clique of size $k$, then its complement $G'$ has a vertex cover of size $|V| - k$.
  * Transformation takes polynomial time.

---

## 4) **Conclusion**

* Since:

  1. Vertex Cover ∈ NP
  2. CLIQUE ≤p Vertex Cover
* ⇒ **Vertex Cover is NP-Complete**.

---

## 5) **Diagram (Quick Visual)**

```
  CLIQUE (NP-Complete)
        │  reduction in polynomial time
        ▼
  VERTEX COVER  (NP-Complete)
```

---

✅ **Final One-Liner (Exam-Ready)**:
*A problem is NP-Complete if it lies in NP and every NP problem reduces to it. Vertex Cover is NP-Complete because it belongs to NP (verification is polynomial) and is reducible from the NP-Complete CLIQUE problem in polynomial time.*

---
