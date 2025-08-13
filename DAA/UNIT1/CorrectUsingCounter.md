
*"How to prove that an algorithm is correct? How to prove correctness using counter example? Give suitable example"* 

---

# **Proving Algorithm Correctness**

## **1. Definition**

* **Correct Algorithm**: Produces the **expected output** for **all valid inputs** and terminates.
* **Correctness Proof** ensures the algorithm **always** works, not just for some inputs.

---

## **2. Methods to Prove Correctness**

### **(i) Mathematical Proof (Loop Invariant / Induction)**

* **Initialization** → Prove it works for the base case.
* **Maintenance** → Show property holds after each step.
* **Termination** → Show final state gives correct output.

### **(ii) Counter Example**

* **Idea**: To prove an algorithm is **incorrect**, it is enough to show **one input** for which it fails.
* Used for **disproving** correctness.
* **Logic**: If an algorithm fails for at least one valid case, it’s not correct for all inputs.

---

## **3. Steps to Use Counter Example**

1. Understand the algorithm’s intended purpose.
2. Identify a case where its logic will break.
3. Provide the **input**, the algorithm’s **output**, and the **expected correct output**.
4. Conclude the algorithm is incorrect.

---

## **4. Example – Counter Example**

**Algorithm (Claimed)**:

> "To find the maximum of three numbers, always return the third number."

**Pseudocode:**

```c
max3(a, b, c):
    return c;
```

**Counter Example:**

* Input: a = 10, b = 50, c = 20
* Algorithm output: 20
* Correct output: 50
* **Conclusion**: Fails for this input → **algorithm is incorrect**.

---

## **5. Real DAA Example – Greedy Approach Failure**

**Problem**: Select coins to make change (coins: 1, 3, 4).
**Algorithm (Claimed)**: Use the largest coin possible at each step (Greedy).

* For change = 6:

  * Greedy picks: 4 + 1 + 1 (3 coins)
  * Optimal: 3 + 3 (2 coins)
* **Counter Example proves Greedy is not optimal** here.

---

## **6. Diagram – Correctness Proof Flow**

```
Algorithm → Test All Inputs? (Not Possible) 
     ↓
Mathematical Proof (If Correct) OR Counter Example (If Incorrect)
```

---

✅ **Exam Tip**:

* For **correctness** → Use **I-M-T** (Initialization–Maintenance–Termination).
* For **incorrectness** → Give **ONE clear counter example** with input, wrong output, correct output.

---

