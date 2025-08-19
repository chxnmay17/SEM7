

---

# SAT, 3-SAT & NP-Completeness of 3-SAT

## 1) Definitions

* **SAT (Boolean Satisfiability)**
  Given a Boolean formula Φ over variables $x_1,\dots,x_n$, decide whether there exists a truth assignment making Φ **true**.
  *Cook–Levin Theorem*: **SAT is NP-complete.**

* **3-SAT (3-CNF-SAT)**
  A **restriction of SAT** where Φ is in **Conjunctive Normal Form (CNF)** and **each clause has exactly 3 literals** (e.g., $(x \lor \lnot y \lor z)$).
  **Decision**: Is there an assignment that satisfies all 3-literal clauses?

---

## 2) 3-SAT is in NP (Membership)

* Given an assignment, we can check each 3-literal clause in **O(1)** and all clauses in **O(m)** (m = #clauses) → **polynomial time verification**.
  ⇒ **3-SAT ∈ NP**.

---

## 3) NP-Completeness of 3-SAT (Proof Outline)

To prove NP-complete: **(i) in NP** (above) **+ (ii) NP-hard** via **polynomial-time reduction** from a known NP-complete problem.
We reduce **SAT ≤p 3-SAT**.

### Reduction idea (CNF-SAT → 3-CNF-SAT):

Transform any CNF clause with length ≠ 3 into an **equivalent** set of 3-literal clauses using fresh variables. The overall formula is satisfiable **iff** the transformed one is.

#### Clause normalization rules

Let clause $C$ contain literals $a_1,\dots,a_k$.

* **If k = 1**: $(a_1)$  →  $(a_1 \lor a_1 \lor a_1)$.
* **If k = 2**: $(a_1 \lor a_2)$  →  $(a_1 \lor a_2 \lor a_2)$.
* **If k = 3**: keep as is.
* **If k ≥ 4 (chain with new vars $y_1,\dots,y_{k-3}$)**:

  $$
  (a_1 \lor a_2 \lor y_1) \;\land\; (\lnot y_1 \lor a_3 \lor y_2)\;\land\;\dots\;\land\;(\lnot y_{k-4} \lor a_{k-2} \lor y_{k-3}) \;\land\; (\lnot y_{k-3} \lor a_{k-1} \lor a_k)
  $$
* **Size & time**: introduces at most $k-3$ new variables/clauses per long clause → **linear blow-up**, overall **polynomial time**.

#### Correctness (equivalence) sketch

* **(⇒)** If original clause $C$ is satisfied, pick truth values for the $y_i$’s to make the chain true (choose $y_i$ to “pass along” the first true literal encountered).
* **(⇐)** If the 3-CNF chain is satisfied, the structure forces that at least one $a_j$ must be true; otherwise some link $(\lnot y_i \lor \dots)$ fails.
  Thus, each clause is preserved in satisfiability, and conjunction over all clauses preserves satisfiability of Φ.

**Therefore**: SAT ≤p 3-SAT. Since SAT is NP-complete and the reduction is polynomial, **3-SAT is NP-hard**. Combined with **3-SAT ∈ NP**, we get **3-SAT is NP-complete**.

---

## 4) Worked Example (one long clause)

Original CNF clause: $(x \lor \lnot y \lor z \lor w)$ (k = 4).
Introduce $y_1$:

$$
(x \lor \lnot y \lor y_1)\ \land\ (\lnot y_1 \lor z \lor w)
$$

Both 3-literal clauses. The pair is satisfiable **iff** the original clause is.

---

## 5) Why 3-SAT matters (DAA takeaway)

* **Canonical NP-complete** problem used as a **source for reductions** to scheduling, graph, and layout problems.
* **Constraint satisfaction** template with exactly 3 literals per clause simplifies reductions.
* Underpins typical “hardness” proofs in exams/projects.

---

## 6) Quick diagram (reduction flow)

```
SAT (NP-complete)
      |
   poly-time
   reduction
      v
   3-SAT
 (in NP)  → NP-complete
```

---

## 7) Exam Mnemonic — **“NPC by 2 steps: Verify + Reduce”**

* **Verify** (membership): 3-SAT ∈ NP (check assignment fast).
* **Reduce** (hardness): SAT ≤p 3-SAT via clause-to-3-clause chaining.

---

