
*"Write a short note on any four problem solving strategies"* 

---

# **Problem Solving Strategies in DAA**

**Definition:**
In DAA, a **problem solving strategy** is a general approach used to design an algorithm that solves a problem efficiently and correctly.

---

## **1. Divide and Conquer**

* **Idea**: Break the problem into smaller subproblems, solve each independently, and combine results.
* **Steps**:

  1. **Divide** – Split into smaller instances.
  2. **Conquer** – Solve recursively.
  3. **Combine** – Merge sub-results into the final solution.
* **Examples**:

  * Merge Sort, Quick Sort, Binary Search.
* **Diagram**:

```
Problem → Divide → Subproblem 1, Subproblem 2 → Solve → Combine → Solution
```

---

## **2. Greedy Method**

* **Idea**: Make the **locally optimal choice** at each step, hoping to find the global optimum.
* **When to Use**: Works well for **optimization problems** with **greedy-choice property** and **optimal substructure**.
* **Examples**:

  * Kruskal’s & Prim’s MST algorithms, Huffman coding.
* **Real-world analogy**: Always pick the **shortest available path** when travelling to save time.

---

## **3. Dynamic Programming (DP)**

* **Idea**: Solve complex problems by **breaking them into overlapping subproblems**, storing results to avoid recomputation.
* **Steps**:

  1. Define **subproblems**.
  2. **Store** results (memoization/tabulation).
  3. Build the solution from stored results.
* **Examples**:

  * Fibonacci sequence, Matrix Chain Multiplication, Longest Common Subsequence.
* **Diagram** (Overlapping subproblems):

```
      Problem
     /      \
  Sub1     Sub2
    \      /
     Common
```

---

## **4. Backtracking**

* **Idea**: Try building the solution step-by-step; if a step leads to a **dead end**, backtrack and try another path.
* **When to Use**: Problems with **constraints** and **multiple possible solutions**.
* **Examples**:

  * N-Queens problem, Sudoku solver, Graph coloring.
* **Code snippet** (N-Queens simplified):

```c
if (safe(row, col)) {
    placeQueen(row, col);
    if (solve(nextRow)) return true;
    removeQueen(row, col); // backtrack
}
```

---

## **Quick Mnemonic to Remember** – **DGDB**

* **D** → Divide & Conquer
* **G** → Greedy
* **D** → Dynamic Programming
* **B** → Backtracking

---

✅ **Exam Tip**: Always write **definition → key steps → examples → diagram** for each strategy to get full marks.

---
