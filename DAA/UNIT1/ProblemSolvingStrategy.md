
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
# **More Detailed**

---

## **Divide and Conquer (Detailed Explanation)**

### **Idea:**

Divide and Conquer is a fundamental algorithm design paradigm. The core idea is to **break a large problem** into smaller subproblems, **solve** each of those subproblems **recursively**, and then **combine** their solutions to get the answer to the original problem.

---

### **Steps:**

#### **1. Divide:**

* Split the problem into **smaller subproblems** of the same type.
* Ideally, the subproblems are **smaller instances** of the original.
* This step often reduces the size of the input by half or more.

**Example:**
In Merge Sort, an array is divided into two halves.

#### **2. Conquer:**

* **Recursively solve** each subproblem.
* If a subproblem is small enough (base case), solve it directly.

**Example:**
In Binary Search, the algorithm recursively (or iteratively) searches one half of the array based on a condition.

#### **3. Combine:**

* Combine the solutions of the subproblems to form the solution to the original problem.
* This step is crucial and can range from trivial (as in Binary Search) to complex (as in Merge Sort).

**Example:**
In Merge Sort, two sorted halves are merged into a fully sorted array.

---

### **Diagram:**

```
        Problem
           |
        Divide
           ↓
 ┌───────────────┐
 │ Subproblem 1  │
 │ Subproblem 2  │
 └───────────────┘
     ↓       ↓
  Solve   Solve (Recursively)
     ↓       ↓
    Combine Results
           ↓
        Solution
```

---

### **When to Use Divide and Conquer:**

* The problem can naturally be broken into smaller subproblems.
* The subproblems are independent and can be solved in isolation.
* The combination of subproblem solutions is straightforward or efficient.

---
Great! Let’s expand the concept of the **Greedy Method** in more detail, with clear explanations, examples, and when to use it.

---

## ⚡ **Greedy Method – Detailed Explanation**

### 💡 **Core Idea:**

The Greedy Method is an algorithmic strategy that makes the **locally optimal choice** at each step, with the hope that this leads to a **globally optimal solution**.

It does **not** backtrack or reconsider previous choices.

---

### 📌 **Key Characteristics:**

1. **Greedy-choice property**:
   A global optimum can be arrived at by selecting a local optimum at each step.

2. **Optimal substructure**:
   An optimal solution to the problem contains optimal solutions to its subproblems.

> ✅ If both properties hold, a greedy algorithm can give the correct answer.

---

### 🧠 **How It Works (General Steps):**

1. **Initialize** the solution (empty or starting point).
2. **Sort or prioritize** choices based on a greedy criterion (e.g. lowest cost, highest value).
3. **Iterate** through the choices:

   * At each step, pick the **best available option** (local optimum).
   * If it's valid, include it in the solution.
4. **Repeat** until a complete solution is formed.



### 🧪 **Example : Kruskal’s Algorithm (Minimum Spanning Tree)**

**Problem:**
Connect all nodes in a graph with the minimum total edge weight.

**Greedy Strategy:**

* Sort all edges by weight.
* Add the **smallest edge** that doesn't form a cycle.
* Repeat until all nodes are connected.



### 🌍 **Real-World Analogy**

> You want to visit several places with the **least total time**.
> So, at every step, you pick the **nearest unvisited location**.

This may work well — but not always. Greedy doesn’t check if a better overall route exists.


### ✅ **When to Use Greedy:**

* Problem has **greedy-choice property**.
* Problem has **optimal substructure**.
* You want an **efficient** solution and **can prove** it’s correct.
* You need a **fast approximation** (even if not optimal).

---

### ⚠️ **When Greedy Fails:**

Greedy algorithms **may not give the optimal solution** if:

* Earlier choices limit future options.
* The problem lacks optimal substructure.

**Example where greedy fails:**

* **0/1 Knapsack problem** — Greedy may choose high-value items too early and miss better combinations.

---




