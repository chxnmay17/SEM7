

---

# P, NP, NP-Hard, NP-Complete Problems

## 1) **P (Polynomial time problems)**

* Class of decision problems **solvable in polynomial time**.
* Efficient algorithms exist → deterministic Turing Machine can solve in ≤ O(nᵏ).
* **Example**:

  * Sorting (O(n log n))
  * Shortest Path (Dijkstra’s)

---

## 2) **NP (Nondeterministic Polynomial time problems)**

* Problems whose **solutions can be verified** in polynomial time, even if not solvable in polynomial time.
* Verifier-based definition: If given a “certificate” (candidate solution), it can be checked in O(nᵏ).
* **Example**:

  * Hamiltonian Path Problem
  * Boolean Satisfiability (SAT)

---

## 3) **NP-Hard**

* Problems at least as hard as NP problems.
* **Not required to be in NP** (may not be verifiable in polynomial time).
* If any NP-hard problem is solved in polynomial time → all NP problems can be solved in polynomial time.
* **Example**:

  * Halting Problem
  * Travelling Salesman (optimization version)

---

## 4) **NP-Complete (NPC)**

* Subset of NP that are also NP-hard.
* Formal: A problem **X** is NP-complete if:

  1. $X \in NP$
  2. Every problem in NP is reducible to $X$ in polynomial time.
* **Significance**: First such problem = **SAT (Cook–Levin Theorem)**.
* **Examples**:

  * 3-SAT
  * Clique Decision Problem
  * Subset Sum

---

## 5) **Diagram (Exam-Favorite)**

```
       NP-Hard
     ┌──────────┐
     │          │
     │   NP     │  (verifiable in poly time)
 ┌───┼──────┐   │
 │ P │      │   │
 └───┘      │   │
     └───NPC────┘
```

---

## 6) **Summary Table**

| Class           | Solvable in Poly Time | Verifiable in Poly Time | Example                    |
| --------------- | --------------------- | ----------------------- | -------------------------- |
| **P**           | ✅ Yes                 | ✅ Yes                   | Sorting, Shortest Path     |
| **NP**          | ❌ Not known           | ✅ Yes                   | SAT, Hamiltonian Path      |
| **NP-Hard**     | ❌ Not required        | ❌ Not required          | Halting Problem, TSP (opt) |
| **NP-Complete** | ❌ Not known           | ✅ Yes                   | 3-SAT, Clique, Subset Sum  |

---

## 7) **Exam Mnemonic – "P ⊆ NP; NPC = NP ∩ NP-Hard"**

* **P** → Easy to solve.
* **NP** → Easy to verify.
* **NP-Hard** → At least as hard as NP.
* **NP-Complete** → Hardest problems in NP.

---

✅ **Final Answer (One-liner)**: *P are efficiently solvable problems, NP are efficiently verifiable problems, NP-Hard are at least as hard as NP (not necessarily in NP), and NP-Complete are the hardest NP problems (both in NP & NP-Hard).*

---

